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
| Memory | Timetec 16 GB (2 × 8 GB) DDR3L-1600 CL11 installed |
| Storage | Samsung 256 GB M.2 2242 SATA SSD retained |
| Operating system | Ubuntu Server 22.04 LTS |
| Cooling | iCAN K5 five-fan cooling stand purchased |
| Local input | HP 230 wireless keyboard purchased |
| Primary role | Ubuntu infrastructure server |

## Completed Hardware Work

- [x] Laptop acquired.
- [x] Ubuntu Server installed and initially configured.
- [x] Baseline hardware identified.
- [x] Storage form factor physically verified.
- [x] Existing Samsung 256 GB SSD retained.
- [x] Timetec 16 GB DDR3L memory installed.
- [x] Internal hardware cleaned and inspected.

## Storage Decision

A WD Blue SA510 1 TB M.2 SATA SSD was evaluated but found to use the 2280 form factor. Atlas uses a 2242 mounting position, so the replacement drive was not installed.

The existing Samsung 256 GB M.2 2242 SATA SSD remains operational and provides sufficient capacity for the current server role. A larger compatible SSD upgrade will only be considered if measured storage usage justifies the cost.

See: [hardware/storage-decision.md](hardware/storage-decision.md)

## Current Status

### In Progress

- [ ] Capture and sanitize post-upgrade system information.
- [ ] Document completed hardware installation photographs.
- [ ] Validate cooling stand operation.
- [ ] Validate wireless keyboard operation.
- [ ] Install and test USB Ethernet adapter when received.
- [ ] Establish baseline temperatures and performance.

### Planned

- [ ] Install replacement bottom cover.
- [ ] Add an external maintenance monitor.
- [ ] Replace the battery.
- [ ] Complete final reliability testing.
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
