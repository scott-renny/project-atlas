# Storage Compatibility Decision

## Decision

Project Atlas will retain its operational Samsung 256 GB M.2 2242 SATA SSD. The storage-capacity upgrade is deferred until measured usage demonstrates a need.

## Existing Drive

| Property | Value |
|---|---|
| Manufacturer | Samsung |
| Capacity | 256 GB |
| Form factor | M.2 2242 |
| Interface | SATA |
| Status | Installed and operational |

## Evaluated Replacement

| Property | Value |
|---|---|
| Manufacturer | Western Digital |
| Model | WD Blue SA510, WDS100T3B0B |
| Capacity | 1 TB |
| Form factor | M.2 2280 |
| Interface | SATA |
| Result | Physically incompatible |
| Action | Return; never installed |

Although the replacement used the correct SATA interface, its 80 mm length did not match the laptop's 42 mm mounting position. No suitable 2280 mounting standoff was identified. The drive was not forced, adapted, or installed.

## Alternatives Considered

### Buy a 1 TB M.2 2242 SATA SSD

Technically viable, but rejected for now because compatible high-capacity drives are comparatively expensive and the current workload does not require the additional capacity.

### Modify the chassis

Rejected because improvised mounting could reduce reliability or damage the laptop and SSD.

### Use external storage later

Remains available for backups, archives, transfers, or other non-system data.

## Rationale

The existing SSD is compatible, functional, and adequate for Ubuntu Server, administrative tools, lightweight containers, configuration files, and routine logs. Large datasets, backups, media, and long-term archives should use separate storage.

## Lessons Learned

- Matching the interface does not guarantee physical compatibility.
- M.2 devices vary in both interface and module length.
- Connector keying and mounting position must be verified before purchase.
- Hardware should never be forced into place.
- A functional component should be retained when an upgrade offers limited practical value.

## Evidence Handling

Before publishing photographs or screenshots, remove serial numbers, barcodes, service tags, order details, addresses, usernames, hostnames, IP or MAC addresses, SSH fingerprints, and credentials.
