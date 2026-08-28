# Storage Compatibility Decision

## Decision

Project Atlas will keep its original Samsung 256 GB M.2 2242 SATA SSD.

A suitable replacement could not be found for the laptop's M.2 2242 SATA form factor. The original drive is operational and remains the Atlas v1 system drive.

## Original Drive

| Property | Value |
|---|---|
| Manufacturer | Samsung |
| Capacity | 256 GB |
| Form factor | M.2 2242 |
| Interface | SATA |
| Status | Original drive; installed and operational |
| Atlas v1 decision | Retain |

## Evaluated Replacement

| Property | Value |
|---|---|
| Manufacturer | Western Digital |
| Model | WD Blue SA510, WDS100T3B0B |
| Capacity | 1 TB |
| Form factor | M.2 2280 |
| Interface | SATA |
| Result | Physically incompatible |
| Outcome | Never installed |

Although the evaluated replacement used the correct SATA interface, its 80 mm length did not match the laptop's 42 mm mounting position. No suitable 2280 mounting position was available. The drive was not forced, adapted, or installed.

## Replacement Search Outcome

Atlas requires an M.2 2242 SATA drive for a direct internal replacement. M.2 describes several sizes and interfaces, so an M.2 drive is not automatically compatible.

No suitable replacement was identified for the required M.2 2242 SATA combination. Atlas v1 will therefore continue using the original Samsung SSD.

## Alternatives Considered

### Use the purchased M.2 2280 SATA SSD

Rejected because the drive was physically too long for the 2242 mounting position.

### Modify the chassis or improvise a mount

Rejected because an improvised installation could reduce reliability or damage the laptop or SSD.

### Buy another M.2 2242 SATA SSD

No suitable replacement was found. This option may be revisited only if the original drive fails or Atlas v1 storage requirements change.

### Use separate external storage

Remains available for backups, archives, transfers, and other non-system data.

## Rationale

The original SSD is compatible, operational, and adequate for the current Atlas v1 system role. Keeping it avoids an unsafe physical workaround and avoids purchasing another incompatible device.

SSD health, available space, and filesystem condition still require current validation evidence. This validation does not change the decision to retain the drive.

## Lessons Learned

- Matching the SATA interface does not guarantee physical compatibility.
- M.2 devices vary in module length as well as interface.
- Atlas requires the 2242 length for its internal mounting position.
- Connector keying and the mounting position must be verified before purchase.
- Hardware should never be forced or improvised into place.
- A functional original component should be retained when no suitable replacement is available.

## Evidence Handling

Before publishing photographs or screenshots, remove serial numbers, barcodes, service tags, order details, addresses, usernames, hostnames, IP or MAC addresses, SSH fingerprints, and credentials.
