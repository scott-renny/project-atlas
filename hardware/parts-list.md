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
| Processor | Intel Core i7-5600U (2 Cores / 4 Threads) | Installed |
| Memory | 8 GB DDR3L-1600 | Installed |
| Storage | 256 GB M.2 SATA SSD | Installed |
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
| Memory Kit | Timetec | 16 GB Kit (2×8 GB) DDR3L-1600 PC3L-12800 CL11 | Upgrade system memory from 8 GB to 16 GB | July 2026 | ✅ Purchased |
| SSD | Western Digital | WD Blue SA510 1 TB M.2 SATA (WDS100T3B0B) | Replace the original 256 GB SSD with a larger, more reliable 1 TB drive | July 18, 2026 | ✅ Purchased |
| Cooling Stand | iCAN | Notebook Cooler K5 Blue (5 Fans with LCD Control Panel) | Improve cooling performance during continuous operation | July 2026 | ✅ Purchased |
| Wireless Keyboard | HP | HP 230 Wireless Keyboard (3L1E7AA#ABA) | Local administration and maintenance | July 2026 | ✅ Purchased |

---

# Planned Hardware

These components are planned for future installation.

| Component | Purpose | Priority | Status |
|-----------|---------|----------|--------|
| USB Gigabit Ethernet Adapter | Replace failed onboard Ethernet port | High | Planned |
| Dedicated External Monitor | Local maintenance console | Medium | Planned |
| Replacement Battery | Restore battery health | Low | Future Upgrade |
| Replacement Bottom Cover | Improve physical appearance | Low | Future Upgrade |

---

# Components Not Required

The following components have intentionally been excluded from Project Atlas.

| Component | Reason |
|-----------|--------|
| Wireless Mouse | Server management will primarily be performed through SSH and command-line administration. |
| Replacement Internal LCD | The failing display will be replaced functionally with a dedicated external monitor. |
| Docking Station | Not required for the intended infrastructure server role. |

---

# Hardware Upgrade Summary

| Component | Original Configuration | Upgraded Configuration |
|-----------|------------------------|------------------------|
| Memory | 8 GB DDR3L | 16 GB Timetec DDR3L |
| Storage | 256 GB M.2 SATA SSD | 1 TB WD Blue SA510 M.2 SATA SSD |
| Cooling | Factory Cooling | iCAN 5-Fan Notebook Cooler |
| Console | Internal LCD Only | External Monitor + HP 230 Wireless Keyboard |
| Networking | Failed Onboard Ethernet | USB Gigabit Ethernet Adapter (Planned) |

---

# Planned Installation Order

1. Capture baseline system information.
2. Photograph the laptop.
3. Install the WD Blue SA510 SSD.
4. Install the Timetec 16 GB memory kit.
5. Verify BIOS hardware detection.
6. Boot Ubuntu Server.
7. Validate storage and memory upgrades.
8. Install the iCAN cooling stand.
9. Configure the HP 230 wireless keyboard.
10. Configure the USB Gigabit Ethernet adapter.
11. Configure the external monitor.
12. Replace the battery (future).
13. Replace the bottom cover (future).

---

# Hardware Status

| Component | Purchased | Installed | Tested |
|-----------|:---------:|:---------:|:------:|
| Dell Latitude E7250 | ✅ | ✅ | ✅ |
| Original 256 GB SSD | ✅ | ✅ | ✅ |
| Timetec 16 GB Memory Kit | ✅ | ⬜ | ⬜ |
| WD Blue SA510 1 TB SSD | ✅ | ⬜ | ⬜ |
| iCAN Notebook Cooler K5 Blue | ✅ | ⬜ | ⬜ |
| HP 230 Wireless Keyboard | ✅ | ⬜ | ⬜ |
| USB Gigabit Ethernet Adapter | ⬜ | ⬜ | ⬜ |
| External Monitor | ⬜ | ⬜ | ⬜ |
| Replacement Battery | ⬜ | ⬜ | ⬜ |
| Replacement Bottom Cover | ⬜ | ⬜ | ⬜ |

---

# Documentation References

Related documentation:

- `hardware/original-specifications.md`
- `hardware/compatibility-notes.md`
- `hardware/upgrade-plan.md`
- `hardware/installation-guide.md`
- `hardware/final-specifications.md`
- `logs/build-log.md`

---

# Supporting Media

## Product Screenshots

```
screenshots/
└── 01-purchased-components/
    ├── wd-blue-sa510-1tb.png
    ├── timetec-16gb-ddr3l-kit.png
    ├── ican-notebook-cooler-k5-blue.png
    └── hp-230-wireless-keyboard.png
```

## Build Photos

```
photos/
├── 01-initial-assessment/
├── 02-disassembly/
├── 03-installation/
└── 04-final-build/
```

---

# Notes

Project Atlas documents the complete restoration and modernization of a Dell Latitude E7250 into a dedicated Ubuntu infrastructure server.

The project emphasizes documentation, validation, and repeatability. Every hardware change is supported by photographs, system screenshots, benchmark results, and engineering notes to provide a complete record of the build from its original state through final deployment.
