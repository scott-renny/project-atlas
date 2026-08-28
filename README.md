# Project Atlas

## Atlas v1 — Dell Latitude E7250 Infrastructure Server

Project Atlas documents the restoration and validation of a Dell Latitude E7250 used as the Ubuntu Server backbone for the COC.

Atlas v1 is the laptop-based platform described in this repository. Atlas v2 is the later 2U rack replacement and is deliberately outside this phase.

## Repository Scope

This repository covers the Atlas v1 host platform: hardware condition and upgrades, operating-system baseline, networking readiness, cooling, local maintenance access, reliability testing, and sanitized evidence.

Detailed application configuration and broader COC architecture remain outside this repository. This phase does not add new services, redesign the COC, or introduce Atlas v2 requirements.

## Confirmed Current State

The latest supplied Atlas audit confirms:

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
| Primary network at audit | Wi-Fi; wired networking not yet validated |
| Remote administration | SSH active |
| Container runtime | Docker active |
| Remote access | WireGuard active |
| Observability | Prometheus, Node Exporter, and Grafana active |
| Security monitoring | Wazuh components active |
| Reverse proxy | Caddy active |

Service names above are inventory evidence only; their detailed configuration belongs with the relevant COC service documentation.

## Completed Hardware Work

- [x] Laptop acquired.
- [x] Ubuntu Server installed and upgraded to 24.04.4 LTS.
- [x] Baseline hardware identified.
- [x] Storage form factor physically verified.
- [x] Existing Samsung 256 GB SSD retained.
- [x] Timetec 16 GB DDR3L memory installed.
- [x] Internal hardware cleaned and inspected.
- [x] Storage compatibility decision recorded.

## Current Repo Phase

The next repository phase is **Atlas v1 platform validation and closeout**.

Its Definition of Done is maintained in [docs/atlas-v1-completion.md](docs/atlas-v1-completion.md). In summary, the phase is complete when:

- confirmed host facts are accurate and consistent across the repository;
- hardware, storage, thermals, power behavior, networking, and local maintenance access have recorded evidence;
- reliability and restart testing have been completed;
- published evidence is sanitized;
- unresolved physical work is either completed or explicitly deferred with a reason;
- the final Atlas v1 specification and known limitations are documented.

## Highest-Priority Incomplete Work

1. Capture a fresh sanitized post-upgrade hardware and operating-system record.
2. Validate a stable wired network path; do not change the live connection until a rollback path is available.
3. Record SSD health, free space, and filesystem evidence.
4. Establish idle and sustained-load temperature baselines.
5. Validate cooling stand and local keyboard operation.
6. Verify lid-close, suspend/hibernate, reboot, and power-recovery behavior for server duty.
7. Complete an extended reliability test and document the outcome.
8. Record final specifications, cost, photographs, and explicitly deferred repairs.

## Storage Decision

A WD Blue SA510 1 TB M.2 SATA SSD was evaluated but found to use the 2280 form factor. Atlas uses a 2242 mounting position, so the replacement drive was not installed.

The operational Samsung 256 GB M.2 2242 SATA SSD remains in service. A larger compatible SSD will only be considered if measured usage justifies the cost.

See [hardware/storage-decision.md](hardware/storage-decision.md).

## Project Boundaries

### Atlas v1

- Dell Latitude E7250 platform
- Ubuntu Server host readiness
- physical restoration and hardware validation
- wired-network readiness
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
