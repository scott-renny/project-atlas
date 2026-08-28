# Original Hardware Specifications

This document preserves the original Atlas baseline and records how each item ended. For the current system state, see the repository README.

## Original System

| Component | Original specification |
|---|---|
| Manufacturer | Dell |
| Model | Latitude E7250 |
| CPU | Intel Core i7-5600U (2 cores / 4 threads) |
| Operating system at original baseline | Ubuntu Server 22.04 LTS |
| Purchase price | $110 CAD |

The supplied current-system audit records Ubuntu Server 24.04.4 LTS and kernel 6.8.0-137-generic.

## Memory

| Item | Outcome |
|---|---|
| Original memory | 8 GB DDR3L |
| Upgrade | Timetec 16 GB (2 × 8 GB) DDR3L-1600 |
| Current status | Installed; recognized by the supplied audit |

## Storage

| Item | Outcome |
|---|---|
| Retained drive | Samsung 256 GB M.2 2242 SATA SSD |
| Status | Installed and operational |
| Capacity upgrade | Deferred until justified |
| Rejected replacement | WD Blue SA510 1 TB M.2 2280 SATA; physically incompatible and never installed |

## Network

| Component | Outcome |
|---|---|
| Wi-Fi | Operational and primary at the supplied audit |
| Bluetooth | Operational at the original baseline |
| Integrated Ethernet | Recorded as non-functional |
| External wired solution | Installed; sustained wired-operation validation pending |

## Display, Input, Cooling, and Repairs

The owner confirms that all planned physical upgrades are complete:

- cooling stand installed;
- wireless keyboard installed;
- external maintenance display path added;
- replacement battery installed;
- replacement bottom cover installed;
- internal hardware cleaned and inspected.

Component details and operational validation evidence remain to be recorded where absent.

## Remaining Validation

- Capture and sanitize a current post-upgrade summary.
- Validate SSD health, free space, and filesystem.
- Validate cooling, keyboard, and local display operation.
- Validate sustained wired networking.
- Validate server-duty power behavior.
- Complete temperature and extended-reliability testing.
- Record final component details, cost, photographs, and known limitations.

The previously observed USB error `-71` should remain documented until its current impact is tested.
