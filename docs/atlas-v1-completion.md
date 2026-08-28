# Atlas v1 Platform Validation and Closeout

## Phase Goal

Validate and document the completed Atlas v1 physical build as a reliable Ubuntu infrastructure platform without expanding into Atlas v2 or adding new COC services.

## Evidence Rules

A checklist item may be marked complete when supported by:

- the supplied system audit;
- the owner's confirmation of completed physical installation; or
- dated, sanitized validation evidence.

Physical installation and operational validation are tracked separately.

## Definition of Done

### 1. Repository Accuracy

- [x] Atlas v1 and Atlas v2 are clearly separated.
- [x] The current operating system is recorded as Ubuntu Server 24.04.4 LTS.
- [x] Physical restoration, cleaning, and maintenance are recorded as complete.
- [x] The current phase is platform validation and closeout.
- [ ] Final component details, specifications, cost, and known limitations are recorded.

### 2. Completed Physical Build

The owner confirms completion of all planned physical upgrades, cleaning, and physical maintenance:

- [x] 16 GB Timetec DDR3L memory installed.
- [x] Internal hardware cleaning, inspection, and physical maintenance completed.
- [x] Samsung 256 GB M.2 2242 SATA SSD retained.
- [x] Cooling stand installed.
- [x] HP 230 wireless keyboard installed.
- [x] External maintenance display path added.
- [x] Battery replaced.
- [x] Bottom cover replaced.

### 3. Host Evidence

- [ ] Add a fresh sanitized post-upgrade system summary.
- [x] Record CPU and installed-memory recognition from the supplied audit.
- [ ] Record disk layout, filesystem usage, and mount points.
- [ ] Record SSD health evidence without serial numbers or other identifiers.
- [x] Record the firmware version from the supplied audit.
- [ ] Record whether the firmware age is an accepted limitation.

### 4. Networking and Remote Administration

- [x] Record that SSH was active during the audit.
- [x] Record that WireGuard was active during the audit.
- [x] Record Wi-Fi as the intentional Atlas v1 production network path.
- [x] Record that no external wired adapter will be installed in Atlas v1.
- [ ] Confirm the Wi-Fi address-assignment method.
- [ ] Confirm SSH key-based administration from another LAN machine.
- [ ] Confirm the remote-access path without publishing addresses, keys, or fingerprints.

### 5. Server-Duty Power Behavior

- [x] Replacement battery installed.
- [ ] Confirm lid close does not suspend the host.
- [ ] Confirm suspend and hibernate behavior is intentionally configured.
- [ ] Confirm a clean reboot returns the host to an administrable state.
- [ ] Record behavior after AC loss and restoration where safely testable.
- [ ] Record battery and charger condition.

### 6. Cooling and Reliability

- [x] Cooling stand installed.
- [ ] Record idle temperatures after a stable settling period.
- [ ] Record temperatures during a repeatable sustained-load test.
- [ ] Record cooling-stand operation under test.
- [ ] Confirm the host remains responsive without thermal shutdowns or throttling.
- [ ] Complete and record an extended reliability run.

### 7. Local Maintenance Access

- [x] Wireless keyboard installed.
- [x] External maintenance display path added.
- [x] Record successful HP 230 keyboard operation at the local Ubuntu console (2026-08-28).
- [ ] Record successful local display operation.
- [ ] Add sanitized photographs of the completed installation where useful.
- [ ] Record the known USB-port limitation and its current operational impact.

### 8. Closeout

- [x] Physical repairs, upgrades, cleaning, and maintenance complete.
- [ ] Record final project cost.
- [ ] Add missing model and specification details for completed components.
- [ ] Add a short rebuild-oriented hardware and host summary.
- [ ] Review all public evidence for sensitive data.
- [ ] Update the changelog and tag the Atlas v1 platform baseline.

## Audit-Supported Current State

The supplied audit confirms:

- Dell Latitude E7250;
- Ubuntu Server 24.04.4 LTS;
- kernel 6.8.0-137-generic;
- Intel Core i7-5600U with four logical CPUs;
- approximately 16 GB of installed memory;
- retained Samsung system SSD;
- 20 days of uptime at collection;
- SSH, Docker, WireGuard, Caddy, Prometheus, Node Exporter, Grafana, and Wazuh components active;
- Wi-Fi was the primary LAN path at collection.

The audit does not establish long-term Wi-Fi test results, temperature results, power-management behavior, SSD health, or local-console test results.

## Evidence Record Template

```markdown
### <validation name>

- Date:
- Result: pass / fail / deferred
- Method:
- Sanitized evidence:
- Known limitations:
- Follow-up:
```

Do not publish usernames, hostnames, addresses, MAC addresses, Wi-Fi details, serial numbers, service tags, SSH fingerprints, private keys, tokens, credentials, or unreviewed terminal output.

## Safe Execution Order

1. Capture the current sanitized baseline.
2. Record the installed physical component details.
3. Validate local display access; keyboard validation is complete.
4. Document the accepted Wi-Fi-only Atlas v1 network design and validate continued connectivity.
5. Validate storage health and free space.
6. Measure temperatures and sustained-load behavior.
7. Validate power-management and reboot behavior.
8. Run extended reliability testing.
9. Reconcile cost, final evidence, and known limitations.
10. Tag the completed Atlas v1 platform baseline.

Network and power-management changes can interrupt access. Atlas v1 remains on Wi-Fi; perform any related changes only when local recovery access is available.
