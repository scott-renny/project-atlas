# Hardware Bill of Materials (BOM)

## Purpose

This document serves as the official Bill of Materials (BOM) for Project Atlas.

It records every hardware component purchased or planned for the restoration and modernization of the Dell Latitude E7250. Each item includes its intended purpose, current installation status, and relevant notes to provide a complete inventory throughout the life of the project.

---

# System Information

| Item | Value |
|------|-------|
| Project | Project Atlas |
| System | Dell Latitude E7250 |
| Primary Role | Ubuntu Infrastructure Server |
| Repository | Project Atlas |
| Last Updated | July 2026 |

---

# Installed Hardware

These components are currently installed in the laptop before any upgrades.

| Component | Current Specification | Status |
|-----------|----------------------|--------|
| Processor | Intel Core i7-5600U | Installed |
| Memory | 8 GB DDR3L | Installed |
| Storage | Existing M.2 SATA SSD | Installed |
| Wireless Adapter | Factory Dell Wi-Fi | Installed |
| Cooling | Factory Cooling System | Installed |
| Display | Internal LCD | Installed (Failing) |
| Battery | Original Dell Battery | Installed |
| Bottom Cover | Original Dell Bottom Cover | Installed |

---

# Purchased Upgrade Components

The following hardware has already been purchased for Project Atlas.

| Component | Manufacturer | Model / Specification | Purpose | Status |
|-----------|--------------|----------------------|---------|--------|
| Memory Kit | Timetec | 16 GB Kit (2 × 8 GB) DDR3L-1600 PC3L-12800 1.35V CL11 | Increase available system memory | Purchased |
| SSD | Timetec | 1 TB M.2 SATA III 2280 SSD (3D NAND TLC) | Increase storage capacity and improve reliability | Purchased |
| Cooling Stand | Multi-Fan Laptop Cooling Stand | Model TBD | Improve airflow and reduce operating temperatures | Purchased |

---

# Planned Hardware

The following components are planned but have not yet been purchased.

| Component | Purpose | Priority | Status |
|-----------|---------|----------|--------|
| Wireless Keyboard | Local command-line administration | High | Planned |
| USB Gigabit Ethernet Adapter | Replace failed onboard Ethernet | High | Planned |
| External Monitor | Dedicated maintenance console | Medium | Planned |
| Replacement Battery | Restore battery health | Low | Future Upgrade |
| Replacement Bottom Cover | Restore cosmetic condition | Low | Future Upgrade |

---

# Components Not Required

The following hardware has intentionally been excluded from Project Atlas.

| Component | Reason |
|-----------|--------|
| Wireless Mouse | Ubuntu Server is administered entirely through the command line. |
| Replacement Internal LCD | A dedicated external monitor will be used instead. |
| Docking Station | Not required for the intended server role. |

---

# Hardware Upgrade Order

The planned installation sequence is:

1. Install the new Timetec 1 TB SSD.
2. Install the Timetec 16 GB DDR3L memory kit.
3. Verify BIOS detects both upgrades.
4. Boot Ubuntu Server.
5. Verify storage and memory are recognized.
6. Install the cooling stand.
7. Configure the wireless keyboard.
8. Configure the USB Gigabit Ethernet adapter.
9. Configure the dedicated external monitor.
10. Replace the battery (future).
11. Replace the bottom cover (future).

---

# Component Inventory

| Component | Purchased | Installed | Tested |
|-----------|-----------|-----------|--------|
| Timetec 16 GB DDR3L Kit | ✅ | ⬜ | ⬜ |
| Timetec 1 TB SATA SSD | ✅ | ⬜ | ⬜ |
| Cooling Stand | ✅ | ⬜ | ⬜ |
| Wireless Keyboard | ⬜ | ⬜ | ⬜ |
| USB Ethernet Adapter | ⬜ | ⬜ | ⬜ |
| External Monitor | ⬜ | ⬜ | ⬜ |
| Replacement Battery | ⬜ | ⬜ | ⬜ |
| Replacement Bottom Cover | ⬜ | ⬜ | ⬜ |

---

# Notes

This Bill of Materials will be updated throughout Project Atlas as components are purchased, installed, tested, and validated.

Each completed installation will be documented with supporting photographs, test results, and references in the project build log.
