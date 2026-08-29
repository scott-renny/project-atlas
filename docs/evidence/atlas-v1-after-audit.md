# Atlas v1 Sanitized Post-Upgrade Audit

This is the public-safe “after” record for Atlas v1. It is derived from the later read-only audit and intentionally omits the hostname, addresses, hardware identifiers, filesystem UUIDs, and other sensitive values.

## Confirmed Platform

| Area | Post-upgrade state |
|---|---|
| Hardware | Dell Latitude E7250 |
| Operating system | Ubuntu Server 24.04.4 LTS |
| Kernel | Linux 6.8.0-137-generic |
| Processor | Intel Core i7-5600U, 2 cores / 4 threads |
| Memory | Approximately 16 GB installed |
| System storage | Retained Samsung 256 GB M.2 2242 SATA SSD |
| Backup storage | Approximately 4 TB, mounted at `/mnt/backup` |
| Uptime at collection | 20 days |
| Primary network | Wi-Fi by design for Atlas v1 |
| Wired networking | Not planned for Atlas v1 |
| Administration | SSH active |
| Remote access | WireGuard active |
| Containers | Docker active |
| Reverse proxy | Caddy active |
| Observability | Prometheus, Node Exporter, and Grafana active |
| Security monitoring | Wazuh components active |

## Storage Snapshot

The audit showed the approximately 250 GB system disk with ample free space and the approximately 4 TB backup disk mounted at `/mnt/backup`. This confirms layout, capacity, and mounts; it does not replace a SMART/SSD health test.

## Evidence Boundary

The terminal screenshots in the photo gallery show the earlier Ubuntu 22.04 / 8 GB pre-upgrade state. They are pre-upgrade evidence. The table above is the authoritative public “after” summary for the finished Atlas v1 platform.

## Still Not Proven by This Audit

- SSD SMART health;
- idle and sustained-load temperatures;
- lid-close and suspend/hibernate behavior;
- reboot and AC-restoration behavior;
- extended reliability results;
- successful local display operation.
