# Hardware Bill of Materials (BOM)

## Purpose

This document serves as the official Bill of Materials (BOM) for Project Atlas.

It records every hardware component that has been installed, purchased, or planned during the restoration and modernization of the Dell Latitude E7250. Each component includes its purpose, status, and relevant notes to provide a complete hardware inventory throughout the project's lifecycle.

---

# Project Information

| Item | Value |
|------|-------|
| Project | Project Atlas |
| System | Dell Latitude E7250 |
| Primary Role | Ubuntu Infrastructure Server |
| Repository | project-atlas |
| Last Updated | July 2026 |

---

# Original System Configuration

The following hardware was installed when the laptop was acquired.

| Component | Specification | Status |
|-----------|---------------|--------|
| Processor | Intel Core i7-5600U | Installed |
| Memory | 8 GB DDR3L | Installed |
| Storage | Existing M.2 SATA SSD | Installed |
| Wireless Adapter | Dell Wireless Adapter | Installed |
| Cooling | Factory Cooling System | Installed |
| Display | Internal LCD | Installed (Failing) |
| Battery | Original Dell Battery | Installed |
| Bottom Cover | Original Dell Bottom Cover | Installed |

---

# Purchased Upgrade Components

The following hardware has already been purchased for Project Atlas.

| Component | Manufacturer | Model | Purpose | Purchase Date | Status |
|-----------|--------------|-------|---------|---------------|--------|
| Memory Kit | Timetec | 16 GB Kit (2×8 GB) DDR3L-1600 PC3L-12800 CL11 | Increase system memory to 16 GB | July 2026 | Purchased |
| SSD | Western Digital | WD Blue SA510 1 TB M.2 SATA SSD (WDS100T3B0B) | Increase storage capacity and improve reliability | July 18, 2026 | Purchased |
| Cooling Stand | Multi-Fan Laptop Cooling Stand | Model TBD | Improve airflow and reduce operating temperatures | July 2026 | Purchased |

---

# Planned Hardware

The following components are planned but have not yet been purchased.

| Component | Purpose | Priority | Status |
|-----------|---------|----------|--------|
| Wireless Keyboard | Local command-line administration | High | Planned |
| USB Gigabit Ethernet Adapter | Replace failed onboard Ethernet controller | High | Planned |
| Dedicated External Monitor | Local maintenance console | Medium | Planned |
| Replacement Battery | Restore battery health | Low | Future Upgrade |
| Replacement Bottom Cover | Restore physical condition | Low | Future Upgrade |

---

# Components Not Required

The following hardware has intentionally been excluded from Project Atlas.

| Component | Reason |
|-----------|--------|
| Wireless Mouse | Ubuntu Server is administered entirely through the command line. |
| Replacement Internal LCD | A dedicated external monitor will be used instead of replacing the failing laptop display. |
| Docking Station | Not required for the intended server role. |

---

# Planned Installation Order

The hardware upgrades will be completed in the following order:

1. Install the WD Blue SA510 1 TB SSD.
2. Install the Timetec 16 GB DDR3L memory kit.
3. Verify BIOS detects the new hardware.
4. Boot Ubuntu Server.
5. Verify memory and storage within Ubuntu.
6. Install the multi-fan cooling stand.
7. Configure the wireless keyboard.
8. Configure the USB Gigabit Ethernet adapter.
9. Configure the dedicated external monitor.
10. Replace the battery (future upgrade).
11. Replace the bottom cover (future upgrade).

---

# Component Status

| Component | Purchased | Installed | Tested |
|-----------|:---------:|:---------:|:------:|
| Timetec 16 GB DDR3L Memory Kit | ✅ | ⬜ | ⬜ |
| WD Blue SA510 1 TB SSD | ✅ | ⬜ | ⬜ |
| Multi-Fan Cooling Stand | ✅ | ⬜ | ⬜ |
| Wireless Keyboard | ⬜ | ⬜ | ⬜ |
| USB Gigabit Ethernet Adapter | ⬜ | ⬜ | ⬜ |
| Dedicated External Monitor | ⬜ | ⬜ | ⬜ |
| Replacement Battery | ⬜ | ⬜ | ⬜ |
| Replacement Bottom Cover | ⬜ | ⬜ | ⬜ |

---

# Future Documentation

As each component is installed, the following will be added to the repository:

- Before and after photographs
- Installation notes
- Compatibility observations
- BIOS verification
- Ubuntu verification
- Benchmark results
- Temperature measurements
- Lessons learned

---

# Notes

Project Atlas is intended to demonstrate the complete restoration and modernization of a used Dell Latitude E7250 into a reliable Ubuntu infrastructure server.

This document will be updated throughout the project as additional hardware is purchased, installed, tested, and validated.
