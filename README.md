# Project Atlas

## Atlas v1 — Dell Latitude E7250 Infrastructure Server

Project Atlas documents the restoration and validation of a Dell Latitude E7250 used as the Ubuntu Server backbone for the COC.

Atlas v1 is the laptop-based platform described in this repository. Atlas v2 is the later 2U rack replacement and is deliberately outside this phase.

## Repository Scope

This repository covers the Atlas v1 host platform: hardware restoration, operating-system baseline, networking readiness, cooling, local maintenance access, reliability testing, power resilience, and sanitized evidence.

Detailed application configuration and broader COC architecture remain outside this repository. This phase does not add new services, redesign the COC, or introduce Atlas v2 requirements.

## Confirmed Current State

The sanitized post-upgrade audit and September 2026 resilience validation confirm:

| Area | Confirmed state |
|---|---|
| Hardware | Dell Latitude E7250 |
| Processor | Intel Core i7-5600U (2 cores / 4 threads) |
| Memory | 16 GB DDR3L installed |
| System storage | Samsung 256 GB M.2 2242 SATA SSD retained |
| Operating system | Ubuntu Server 24.04.4 LTS |
| Kernel | Linux 6.8.0-137-generic at audit |
| Host role | COC infrastructure server |
| Atlas v1 network | Wi-Fi; no external wired adapter will be added in this version |
| Remote administration | SSH active |
| Remote access | WireGuard and Tailscale present; external SSH/remote-development acceptance confirmed by the owner |
| Container runtime | Docker active; production containers configured to recover automatically |
| Power recovery | BIOS Wake on AC enabled and physically validated |
| Battery protection | Battery-backed graceful shutdown watchdog at 35% when AC is absent |
| Security maintenance | Ubuntu security updates automated; disruptive upgrades and reboots controlled |
| Observability | Prometheus, Node Exporter, and Grafana active at audit |
| Security monitoring | Wazuh components active at audit |
| Reverse proxy | Caddy active at audit |

Service names above are inventory and resilience evidence only; their detailed configuration belongs with the relevant COC service documentation.

## Physical Upgrade Status

The project owner has confirmed that all planned physical upgrades, cleaning, and physical maintenance are complete:

- [x] 16 GB Timetec DDR3L memory installed.
- [x] Existing Samsung 256 GB SSD retained after compatibility review.
- [x] Internal hardware cleaning, inspection, and physical maintenance completed.
- [x] Cooling stand installed.
- [x] HP 230 wireless keyboard installed and validated at the local Ubuntu console.
- [x] External maintenance display path added.
- [x] Battery replaced.
- [x] Bottom cover replaced.

Completion above records installation status. Validation results remain separate unless supported by the system audit or published test evidence.

## Reliability and Unattended Operation

Before a three-week period away from home to support a new site and train managers and team leads, Atlas was specifically validated for unattended operation rather than expanded with new features.

The September 7, 2026 resilience milestone proved that:

- a normal reboot returns Atlas to an administrable state;
- restoring AC power after a shutdown causes the system to boot automatically without a physical power-button press;
- the laptop battery can act as a short-duration built-in UPS;
- `atlas-power-watch.timer` checks AC and battery state every minute and cleanly shuts down the host at 35% or below when AC is absent;
- SSH, Docker, systemd-networkd, Tailscale, WireGuard, and the watchdog return after reboot;
- the production Docker containers `daedalus-postgres`, `n8n`, `cadvisor`, `pihole`, and `dockge-dockge-1` recover automatically via `unless-stopped` restart policies;
- Pi-hole returns healthy after reboot;
- the host reaches a clean `running` systemd state with zero failed units;
- Ubuntu security maintenance is automated while potentially disruptive application, container, OS-release, firmware, and reboot changes remain deliberate.

The operating principle is simple: **recovery is automatic, security maintenance is automatic where safe, and potentially disruptive change is deliberate.**

See [docs/evidence/atlas-v1-resilience-validation-2026-09-07.md](docs/evidence/atlas-v1-resilience-validation-2026-09-07.md).

## Current Repo Phase

Atlas v1 is **operational; the September 7, 2026 unattended-operation milestone is complete and closed**. The owner also confirmed successful external-network SSH and remote-development acceptance. Optional evidence and additional validation follow-up do not reopen this milestone or imply those additional tests have passed.

The Definition of Done is maintained in [docs/atlas-v1-completion.md](docs/atlas-v1-completion.md).

## Evidence

- [Sanitized build and restoration photographs](docs/evidence/atlas-v1-build-evidence.md)
- [Sanitized post-upgrade audit summary](docs/evidence/atlas-v1-after-audit.md)
- [Atlas v1 resilience validation — 2026-09-07](docs/evidence/atlas-v1-resilience-validation-2026-09-07.md)

The terminal screenshots in the evidence gallery document the earlier Ubuntu 22.04 / 8 GB baseline. They are historical “before” evidence and are not the finished Atlas v1 state.

## Optional Follow-up — Non-blocking

1. Record SSD health evidence.
2. Establish idle and sustained-load temperature baselines.
3. Record cooling stand and local display validation.
4. Finish any remaining lid-close and suspend/hibernate checks for server duty.
5. Complete an extended reliability test and document the outcome.
6. Record final component details, cost, photographs, and known limitations.

## Storage Decision

A WD Blue SA510 1 TB M.2 SATA SSD was evaluated but found to use the 2280 form factor. Atlas uses a 2242 mounting position, so the replacement drive was not installed.

The operational Samsung 256 GB M.2 2242 SATA SSD remains in service. A larger compatible SSD will only be considered if measured usage justifies the cost.

See [hardware/storage-decision.md](hardware/storage-decision.md).

## Project Boundaries

### Atlas v1

- Dell Latitude E7250 platform
- Ubuntu Server host readiness
- completed physical restoration
- Wi-Fi network validation
- cooling and reliability validation
- unattended power recovery and graceful battery shutdown
- local maintenance access
- sanitized rebuild and closeout evidence

### Not This Phase

- Atlas v2 or 2U rack hardware
- Kubernetes expansion
- new COC applications
- major service redesigns
- detailed service configuration
- unrelated homelab expansion

## Privacy

Public evidence must not expose usernames, hostnames, IP or MAC addresses, Wi-Fi details, serial numbers, service tags, order details, SSH fingerprints, tokens, or credentials. Crop or redact product and installation images before publication.

## License

This project is licensed under the MIT License.
