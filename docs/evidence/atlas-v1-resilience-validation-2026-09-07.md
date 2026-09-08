# Atlas v1 Resilience Validation — 2026-09-07

## Operational Context

This validation was completed before the project owner left home for approximately three weeks to support a new site and train managers and team leads. The operational requirement was straightforward: Atlas needed to continue running unattended, survive ordinary reboots and short power interruptions, and recover automatically after AC power returned without requiring someone to press the power button or manually restart core services.

This work followed the project's simplicity-first rule: reuse the laptop battery, existing systemd capabilities, Docker restart policies, and already-installed remote-access tooling before adding new hardware or software.

## Validation Summary

### Automatic power recovery

- Result: **PASS**
- Dell Latitude E7250 BIOS `Wake on AC` was enabled.
- A cold recovery test was performed by shutting the host down, removing AC power, reconnecting AC power, and **not** pressing the power button.
- Atlas powered on automatically and returned to an administrable state.

### Battery-backed graceful shutdown

- Result: **PASS**
- The replacement laptop battery is used as the built-in short-duration UPS.
- `atlas-power-watch.timer` runs once per minute.
- The watchdog powers the host off cleanly when AC power is absent and battery capacity is at or below 35%.
- Conditional logic was validated safely at representative values: AC present at low battery keeps the host running; AC absent above 35% keeps it running; AC absent at 35% or below selects shutdown.
- The battery was not intentionally drained to 35% solely for testing.

### Reboot and service recovery

- Result: **PASS**
- A normal reboot returned Atlas to an administrable state.
- Final post-reboot system state was `running` with zero failed systemd units.
- SSH, Docker, systemd-networkd, Tailscale, WireGuard, and the Atlas power-watch timer were enabled and active after reboot.
- Production Docker containers recovered automatically using `unless-stopped` restart policies:
  - `daedalus-postgres`
  - `n8n`
  - `cadvisor`
  - `pihole`
  - `dockge-dockge-1`
- Pi-hole specifically returned in a healthy state after reboot.

### Update resilience

- Result: **PASS**
- `unattended-upgrades` and the standard APT maintenance timers are enabled.
- Ubuntu security updates are allowed to install automatically.
- Ordinary potentially disruptive updates, third-party application/container updates, operating-system release upgrades, firmware updates, and automatic reboots remain controlled/manual.
- No reboot was required at the final validation check.

### Cleanup performed during validation

- OpenIPMI was confirmed to have no usable IPMI hardware on the Latitude platform.
- The unused Prometheus IPMI sensor timer was disabled.
- `openipmi.service` was masked to eliminate the false boot failure while remaining reversible.
- The obsolete Docker `hello-world` test container and image were removed.
- Final validation showed zero failed systemd units.

## Result

Atlas v1 passed the pre-travel unattended-operation resilience milestone. The host demonstrated automatic boot after restored AC power, graceful low-battery shutdown logic, successful reboot recovery, persistent core networking/remote-access services, automatic recovery of production containers, and a conservative security-update policy.

The guiding operating principle is:

> Recovery is automatic. Security maintenance is automatic where safe. Potentially disruptive change is deliberate.

## Public Evidence Safety

This record intentionally omits usernames, hostnames used for private administration, IP and MAC addresses, Wi-Fi details, SSH fingerprints, serial numbers, tokens, credentials, and other sensitive infrastructure data.
