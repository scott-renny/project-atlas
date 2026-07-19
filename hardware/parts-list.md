# Hardware Bill of Materials (BOM)

## Purpose

This document serves as the official Bill of Materials (BOM) for Project Atlas.

It tracks every hardware component associated with the restoration and modernization of the Dell Latitude E7250 into a reliable Ubuntu infrastructure server. Each component includes its current status, purpose, and notes to maintain a complete hardware inventory throughout the project's lifecycle.

---

# Project Information

| Item | Value |
|------|-------|
| Project | Project Atlas |
| Repository | project-atlas |
| System | Dell Latitude E7250 |
| Primary Role | Ubuntu Infrastructure Server |
| Last Updated | July 2026 |

---

# Original System Configuration

These components were installed when the laptop was acquired.

| Component | Specification | Status |
|-----------|---------------|--------|
| Laptop | Dell Latitude E7250 | Installed |
| Processor | Intel Core i7-5600U | Installed |
| Memory | 8 GB DDR3L | Installed |
| Storage | Existing M.2 SATA SSD | Installed |
| Wireless Adapter | Dell Wireless Adapter | Installed |
| Cooling | Factory Cooling System | Installed |
| Display | Internal LCD (Failing) | Installed |
| Battery | Original Dell Battery | Installed |
| Bottom Cover | Original Dell Bottom Cover | Installed |
| Ethernet Port | Integrated RJ-45 | Non-Functional |

---

# Purchased Upgrade Components

The following hardware has been purchased for Project Atlas.

| Component | Manufacturer | Model | Purpose | Purchase Date | Status |
|-----------|--------------|-------|---------|---------------|--------|
| Memory Kit | Timetec | 16 GB Kit (2×8 GB) DDR3L-1600 PC3L-12800 CL11 | Upgrade system memory | July 2026 | ✅ Purchased |
| SSD | Western Digital | WD Blue SA510 1 TB M.2 SATA (WDS100T3B0B) | Replace existing storage | July 18, 2026 | ✅ Purchased |
| Cooling Stand | iCAN | Notebook Cooler K5 Blue (5 Fans with LCD Control Panel) | Improve cooling performance | July 2026 | ✅ Purchased |
| Wireless Keyboard | HP | HP 230 Wireless Keyboard (3L1E7AA#ABA) | Local server administration | July 2026 | ✅ Purchased |

---

# Planned Hardware

These components are planned for future installation.

| Component | Purpose | Priority | Status |
|-----------|---------|----------|--------|
| USB Gigabit Ethernet Adapter | Replace failed onboard Ethernet | High | Planned |
| Dedicated External Monitor | Local maintenance console | Medium | Planned |
| Replacement Battery | Restore battery life | Low | Future Upgrade |
| Replacement Bottom Cover | Improve physical condition | Low | Future Upgrade |

---

# Components Not Required

The following components have intentionally been excluded from Project Atlas.

| Component | Reason |
|-----------|--------|
| Wireless Mouse | Ubuntu Server will be administered primarily through the command line using SSH or a keyboard. |
| Replacement Internal Display | The failing LCD will be replaced by a dedicated external monitor during maintenance. |
| Docking Station | Not required for the intended server role. |

---

# Planned Installation Order

The hardware upgrades will be completed in the following order.

1. Document baseline system state.
2. Install the WD Blue SA510 SSD.
3. Install the Timetec 16 GB memory kit.
4. Verify BIOS hardware detection.
5. Boot Ubuntu Server.
6. Verify memory and storage within Ubuntu.
7. Install and configure the cooling stand.
8. Configure the HP 230 wireless keyboard.
9. Configure the USB Gigabit Ethernet adapter.
10. Configure the external monitor.
11. Replace the battery (future).
12. Replace the bottom cover (future).

---

# Hardware Status

| Component | Purchased | Installed | Tested |
|-----------|:---------:|:---------:|:------:|
| Dell Latitude E7250 | ✅ | ✅ | ✅ |
| Timetec 16 GB DDR3L Memory Kit | ✅ | ⬜ | ⬜ |
| WD Blue SA510 1 TB SSD | ✅ | ⬜ | ⬜ |
| iCAN Notebook Cooler K5 Blue | ✅ | ⬜ | ⬜ |
| HP 230 Wireless Keyboard | ✅ | ⬜ | ⬜ |
| USB Gigabit Ethernet Adapter | ⬜ | ⬜ | ⬜ |
| External Monitor | ⬜ | ⬜ | ⬜ |
| Replacement Battery | ⬜ | ⬜ | ⬜ |
| Replacement Bottom Cover | ⬜ | ⬜ | ⬜ |

---

# Documentation References

Supporting documentation for each component can be found in:

- `hardware/original-specifications.md`
- `hardware/compatibility-notes.md`
- `hardware/upgrade-plan.md`
- `hardware/installation-guide.md`
- `logs/build-log.md`

---

# Supporting Media

Product screenshots are stored in:

```
screenshots/
└── 01-purchased-components/
    ├── wd-blue-sa510-1tb.png
    ├── timetec-16gb-ddr3l-kit.png
    ├── ican-notebook-cooler-k5-blue.png
    └── hp-230-wireless-keyboard.png
```

Installation photographs will be stored in:

```
photos/
├── 01-initial-assessment/
├── 02-disassembly/
├── 03-installation/
└── 04-final-build/
```

---

# Notes

Project Atlas documents the complete restoration of a Dell Latitude E7250 into a dedicated Ubuntu infrastructure server.

This document will continue to evolve as additional hardware is purchased, installed, tested, and validated throughout the project's lifecycle.
