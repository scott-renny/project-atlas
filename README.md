# Project Atlas

## Dell Latitude E7250 Hardware Restoration and Server Upgrade

Project Atlas documents the restoration and hardware modernization of a used Dell Latitude E7250 that is being repurposed as a dedicated Ubuntu infrastructure server.

The project focuses on physical repairs, hardware upgrades, cooling, local console access, testing, and long-term reliability. Software services and the broader homelab architecture are documented separately in the main homelab repository.

---

## Project Objective

The objective of Project Atlas is to extend the usable life of an older business-class laptop and convert it into a dependable command-line server for a cybersecurity homelab.

The system will normally be managed remotely through SSH. A wireless keyboard and dedicated external monitor will provide local command-line access when maintenance or troubleshooting is required.

---

## Base System

| Component | Original Specification |
|---|---|
| Manufacturer | Dell |
| Model | Latitude E7250 |
| Processor | Intel Core i7-5600U |
| Memory | 8 GB |
| Operating System | Ubuntu Server 22.04 LTS |
| Purchase Price | $110 CAD |
| Primary Role | Ubuntu infrastructure server |

---

## Known Issues

The laptop was purchased as a used system and currently has several hardware and cosmetic concerns:

- The internal laptop display is nearing the end of its usable life.
- The integrated Ethernet port has a hardware failure.
- One USB port has previously generated USB error `-71`.
- The bottom cover requires replacement.
- The battery will require replacement.
- The current memory capacity is limited to 8 GB.
- The current SSD will be replaced or upgraded.

These issues will be documented, repaired, bypassed, or monitored throughout the project.

---

## Project Scope

Project Atlas covers the following work:

### Hardware Upgrades

- Upgrade the system from 8 GB to 16 GB of DDR3L memory.
- Install a larger M.2 SATA SSD.
- Inspect and clean the internal cooling system.
- Replace the processor thermal compound if required.
- Verify memory, storage, temperatures, and system stability.

### Physical Restoration

- Replace the bottom cover at a later stage.
- Replace the battery at a later stage.
- Inspect missing or damaged screws and rubber feet.
- Document the physical condition before and after restoration.

### Cooling and Placement

- Install the laptop on a multi-fan cooling stand.
- Measure temperatures before and after using the cooling stand.
- Keep the server in a stable, ventilated desktop location.
- Organize the power, network, monitor, and keyboard cables.

### Local Command-Line Console

- Add a wireless keyboard for local command-line administration.
- Add a dedicated external monitor because the internal display is failing.
- Configure the system so that normal administration is performed over SSH.
- Retain the external display as a maintenance and recovery console.

### Network Connectivity

- Use a USB Gigabit Ethernet adapter to bypass the failed onboard Ethernet port.
- Verify stable wired network connectivity.
- Document the adapter and network configuration used by the server.

---

## Current Status

### Completed

- [x] Dell Latitude E7250 acquired.
- [x] Ubuntu Server installed.
- [x] Initial server configuration completed.
- [x] Multi-fan laptop cooling stand purchased.

### In Progress

- [ ] Document original system condition.
- [ ] Record current hardware information.
- [ ] Upgrade the SSD.
- [ ] Upgrade the memory to 16 GB.
- [ ] Install and test the cooling stand.
- [ ] Add the wireless keyboard.
- [ ] Test USB Ethernet connectivity.
- [ ] Establish baseline temperatures and performance.

### Planned

- [ ] Add a dedicated external monitor.
- [ ] Replace the battery.
- [ ] Replace the bottom cover.
- [ ] Complete cosmetic restoration.
- [ ] Perform final reliability and stability testing.
- [ ] Record final specifications and total project cost.

---

## Planned Repository Structure

```text
project-atlas/
├── README.md
├── CHANGELOG.md
├── LICENSE
├── docs/
│   ├── project-overview.md
│   ├── initial-assessment.md
│   ├── upgrade-plan.md
│   ├── hardware-installation.md
│   ├── cooling-and-placement.md
│   ├── local-console.md
│   ├── testing-and-validation.md
│   └── lessons-learned.md
├── hardware/
│   ├── original-specifications.md
│   ├── parts-list.md
│   ├── compatibility-notes.md
│   └── final-specifications.md
├── logs/
│   ├── build-log.md
│   ├── benchmark-results.md
│   └── temperature-results.md
├── screenshots/
└── photos/
