# Project Atlas

## Atlas v1 — Dell Latitude E7250 Infrastructure Server

Project Atlas documents the restoration and validation of a Dell Latitude E7250 used as the Ubuntu Server backbone for the COC.

Atlas v1 is the laptop-based platform described in this repository. Atlas v2 is the later 2U rack replacement and is deliberately outside this phase.

## Repository Scope

This repository covers the Atlas v1 host platform: hardware restoration, operating-system baseline, networking readiness, cooling, local maintenance access, reliability testing, and sanitized evidence.

Detailed application configuration and broader COC architecture remain outside this repository. This phase does not add new services, redesign the COC, or introduce Atlas v2 requirements.

## Confirmed Current State

The sanitized post-upgrade audit summary confirms:

| Area | Confirmed state |
|---|---|
| Hardware | Dell Latitude E7250 |
| Processor | Intel Core i7-5600U (2 cores / 4 threads) |
| Memory | 16 GB DDR3L installed |
| System storage | Samsung 256 GB M.2 2242 SATA SSD retained |
| Operating system | Ubuntu Server 24.04.4 LTS |
| Kernel | Linux 6.8.0-137-generic |
| Host role | COC infrastructure server |
| Uptime at audit | 20 days |
| Atlas v1 network | Wi-Fi; no external wired adapter will be added in this version |
| Remote administration | SSH active |
| Container runtime | Docker active |
| Remote access | WireGuard active |
| Observability | Prometheus, Node Exporter, and Grafana active |
| Security monitoring | Wazuh components active |
| Reverse proxy | Caddy active |

Service names above are inventory evidence only; their detailed configuration belongs with the relevant COC service documentation.

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

## Current Repo Phase

Atlas v1 is now in **platform validation and closeout**. Physical restoration, cleaning, and maintenance are complete; the remaining work is to capture sanitized evidence and validate the finished platform.

The Definition of Done is maintained in [docs/atlas-v1-completion.md](docs/atlas-v1-completion.md).

## Evidence

- [Sanitized build and restoration photographs](docs/evidence/atlas-v1-build-evidence.md)
- [Sanitized post-upgrade audit summary](docs/evidence/atlas-v1-after-audit.md)

The terminal screenshots in the evidence gallery document the earlier Ubuntu 22.04 / 8 GB baseline. They are historical “before” evidence and are not the finished Atlas v1 state.

## Highest-Priority Incomplete Work

1. Document Wi-Fi as the intentional Atlas v1 network path and the lack of wired networking as an accepted limitation.
2. Record SSD health evidence.
3. Establish idle and sustained-load temperature baselines.
4. Record cooling stand and local display validation.
5. Verify lid-close, suspend/hibernate, reboot, and power-recovery behavior for server duty.
6. Complete an extended reliability test and document the outcome.
7. Record final component details, cost, photographs, and known limitations.

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
