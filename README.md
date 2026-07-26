# Project Atlas

## Dell Latitude E7250 Hardware Restoration and Server Upgrade

Project Atlas documents the physical restoration and hardware modernization of a used Dell Latitude E7250 being repurposed as a dependable Ubuntu infrastructure server.

The repository focuses on the physical server platform: condition assessment, compatible hardware, cooling, local console access, testing, and long-term reliability. Hosted services and the broader homelab architecture are documented separately.

## Objective

Extend the useful life of an older business-class laptop and prepare it as a reliable, primarily headless command-line server. Routine administration will occur over SSH; a wireless keyboard and future external monitor will provide local maintenance access.

## Current Hardware

| Component | Configuration |
|---|---|
| Model | Dell Latitude E7250 |
| Processor | Intel Core i7-5600U (2 cores / 4 threads) |
| Memory | 8 GB DDR3L; Timetec 16 GB kit purchased |
| Storage | Samsung 256 GB M.2 2242 SATA SSD retained |
| Operating system | Ubuntu Server 22.04 LTS |
| Cooling | Factory cooling; iCAN K5 stand purchased |
| Local input | HP 230 wireless keyboard purchased |
| Primary role | Ubuntu infrastructure server |

## Known Issues

- The internal display is deteriorating.
- The integrated Ethernet port is non-functional.
- One USB port previously generated error `-71`.
- The battery and bottom cover require future replacement.

## Project Scope

- Install and validate the 16 GB DDR3L memory kit.
- Retain and validate the existing 256 GB SSD.
- Clean and assess the internal cooling system.
- Install and test the five-fan cooling stand.
- Add an external maintenance monitor.
- Select and validate a Linux-compatible wired-network solution.
- Replace the battery and bottom cover in later phases.
- Record photographs, benchmarks, temperatures, and stability results.

## Storage Decision

A WD Blue SA510 1 TB M.2 SATA SSD was evaluated but found to use the 2280 form factor. Atlas uses a 2242 mounting position, so the replacement drive was not installed and is being returned.

The existing Samsung 256 GB M.2 2242 SATA SSD remains operational and provides sufficient capacity for the current role. A capacity upgrade is deferred until measured usage justifies a compatible replacement. See [hardware/storage-decision.md](hardware/storage-decision.md).

## Current Status

### Completed

- [x] Laptop acquired.
- [x] Ubuntu Server installed and initially configured.
- [x] Baseline hardware identified.
- [x] Storage form factor physically verified.
- [x] Existing SSD retained.
- [x] Memory kit, cooling stand, and wireless keyboard purchased.

### In Progress

- [ ] Capture and sanitize baseline system information.
- [ ] Document the original physical condition.
- [ ] Install and validate the 16 GB memory kit.
- [ ] Install and test the cooling stand and keyboard.
- [ ] Select and test a wired-network solution.
- [ ] Establish baseline temperatures and performance.

### Planned

- [ ] Add an external monitor.
- [ ] Replace the battery and bottom cover.
- [ ] Complete cosmetic restoration.
- [ ] Perform final reliability testing.
- [ ] Record final specifications and project cost.

## Project Boundaries

Project Atlas remains the physical server restoration project. Homelab architecture, Docker services, security labs, and detailed application configurations are outside this repository.

Project Athena may be tested on Atlas as a possible future workload, but it is not part of Atlas's restoration scope and may later move to dedicated hardware.

## Privacy

Public evidence must not expose usernames, hostnames, IP or MAC addresses, Wi-Fi details, serial numbers, service tags, order details, SSH fingerprints, tokens, or credentials. Crop or redact product and installation images before publication.

## Success Criteria

- The system recognizes and passes testing with 16 GB of memory.
- The retained SSD passes health checks and has adequate free space.
- Temperatures remain acceptable during extended operation.
- Wired networking remains stable.
- The keyboard and external monitor provide a usable local console.
- Future physical repairs and final validation are documented.

## License

This project is licensed under the MIT License.
