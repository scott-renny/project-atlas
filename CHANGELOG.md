# Changelog

All notable Project Atlas updates are documented here.

## 2026-09-10 EDT / 2026-09-11 UTC — Nextcloud service acceptance

- Linked completed COC Phase 9 and recorded Nextcloud security, recovery and reboot persistence acceptance on Atlas.
- Preserved Atlas v1 scope and deferred mobile onboarding; no live configuration change is claimed.

## 2026-09-07 — Operational milestone closed

- Marked Atlas v1 operational and the unattended-operation resilience milestone complete.
- Recorded owner confirmation of successful external-network SSH and remote-development acceptance.
- Classified remaining evidence and additional validation as non-blocking follow-up without claiming unperformed tests passed.

## [Unreleased]

### Added

- Added the Atlas v1 platform validation and closeout Definition of Done.
- Added evidence requirements and a safe execution order for remaining validation.
- Added a clear boundary between Atlas v1 and the later Atlas v2 2U rack replacement.
- Recorded owner confirmation that all planned physical upgrades, cleaning, and physical maintenance are complete.
- Added a formal storage compatibility decision record.
- Added a public-safe, sanitized baseline summary.
- Added privacy guidance for photographs, screenshots, and terminal output.
- Added a sanitized 22-image Atlas v1 evidence gallery.
- Added a sanitized post-upgrade audit summary and clearly separated it from the Ubuntu 22.04 / 8 GB historical screenshots.
- Added a dated Atlas v1 resilience validation record for the 2026-09-07 pre-travel milestone.
- Added a battery-backed graceful-shutdown watchdog that checks AC and battery state every minute and shuts the host down cleanly at 35% or below when AC is absent.

### Changed

- Updated the repository quality workflow to pinned `actions/checkout` v7.0.1.
- Validated HP 230 wireless keyboard operation at the local Ubuntu console.
- Reconciled the current operating system with the supplied Ubuntu Server 24.04.4 LTS audit.
- Preserved Ubuntu Server 22.04 LTS as the original historical baseline.
- Updated the project phase from assessment and physical upgrading to platform validation and closeout.
- Distinguished physical installation from operational validation.
- Updated memory, cooling, keyboard, external display, battery, bottom-cover, cleaning, and maintenance status.
- Retained the operational Samsung 256 GB M.2 2242 SATA SSD.
- Deferred a capacity upgrade until measured usage justifies one.
- Recorded the WD Blue SA510 1 TB M.2 2280 SSD as incompatible and never installed.
- Recorded Wi-Fi as the Atlas v1 network path and the external wired adapter as not installed and intentionally out of scope for this version.
- Clarified that the repository covers Atlas v1 host-platform readiness without absorbing detailed service configuration.
- Enabled and physically validated Dell BIOS `Wake on AC` so Atlas powers itself back on when AC returns.
- Validated a normal reboot and an AC-restoration cold-recovery cycle, including automatic recovery of core host services and production Docker containers.
- Confirmed SSH, Docker, systemd-networkd, Tailscale, WireGuard, and the Atlas power-watch timer return after reboot.
- Confirmed production containers use `unless-stopped` restart policies and recover automatically; Pi-hole returned healthy after reboot.
- Confirmed the final post-reboot systemd state as `running` with zero failed units.
- Confirmed Ubuntu unattended security maintenance is enabled while ordinary potentially disruptive updates, third-party application/container updates, firmware/OS-release changes, and automatic reboots remain controlled.
- Disabled the unused Prometheus IPMI sensor timer and masked the unsupported OpenIPMI boot service after confirming the Latitude platform has no usable IPMI hardware.
- Removed the obsolete Docker `hello-world` test container and image.

### Operational Context

- The resilience work was completed before the project owner left home for approximately three weeks to support a new site and train managers and team leads.
- The requirement was to make Atlas capable of unattended operation and recovery rather than adding new features immediately before travel.
- The operating principle established for Atlas is: recovery is automatic, security maintenance is automatic where safe, and potentially disruptive change is deliberate.

### Optional Follow-up — Non-blocking

- Record missing component models, dates, photographs, and final cost.
- Validate storage health, cooling, remaining local maintenance access, selected lid/suspend behavior, and extended reliability.
- Record final specifications and known limitations.

## [0.1.0] - 2026-07-19

### Added

- Created the repository, README, and project overview.
- Documented the Dell Latitude E7250 baseline.
- Defined the restoration scope and initial success criteria.
- Established SSH as the primary administration method.
