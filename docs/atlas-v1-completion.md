# Atlas v1 Platform Validation and Closeout

## Phase Goal

Close the gap between an operational Atlas host and a documented, reproducible, reliable Atlas v1 platform without expanding into Atlas v2 or adding new COC services.

## Definition of Done

This repository phase is complete when every item below is either:

- marked complete with the date and a link to sanitized evidence; or
- explicitly deferred with the reason, impact, owner, and revisit condition.

### 1. Repository Accuracy

- [x] Atlas v1 and Atlas v2 are clearly separated.
- [x] The repository identifies the current operating system as Ubuntu Server 24.04.4 LTS.
- [x] The current project phase is platform validation and closeout.
- [ ] Hardware and status facts are consistent across all remaining documents.
- [ ] Final specifications and known limitations are recorded.

### 2. Host Evidence

- [ ] Add a fresh sanitized post-upgrade system summary.
- [ ] Record CPU and installed-memory recognition.
- [ ] Record disk layout, filesystem usage, and mount points.
- [ ] Record SSD health evidence without serial numbers or other identifiers.
- [ ] Record relevant firmware version and any accepted firmware risk.

### 3. Networking and Remote Administration

- [ ] Validate the intended wired network adapter and sustained link stability.
- [ ] Confirm the production address-assignment method.
- [ ] Confirm SSH key-based administration from another LAN machine.
- [ ] Confirm the remote-access path without publishing addresses, peer keys, or fingerprints.
- [ ] Document a rollback method before changing the primary network path.

### 4. Server-Duty Power Behavior

- [ ] Confirm lid close does not suspend the host.
- [ ] Confirm suspend and hibernate behavior is intentionally configured.
- [ ] Confirm a clean reboot returns the host to an administrable state.
- [ ] Record behavior after AC loss and restoration where safely testable.
- [ ] Record battery and charger condition or explicitly accept their limitations.

### 5. Cooling and Reliability

- [ ] Record idle temperatures after a stable settling period.
- [ ] Record temperatures during a repeatable sustained-load test.
- [ ] Validate cooling-stand operation.
- [ ] Confirm the host remains responsive and free of thermal shutdowns or throttling during the test.
- [ ] Complete and record an extended reliability run.

### 6. Local Maintenance Access

- [ ] Validate the HP wireless keyboard.
- [ ] Validate a usable local display path.
- [ ] Photograph the completed installation where useful and sanitize images before publication.
- [ ] Record the known USB-port limitation and its operational impact.

### 7. Closeout

- [ ] Record final project cost.
- [ ] Mark physical repairs complete or explicitly deferred.
- [ ] Add a short rebuild-oriented hardware and host summary.
- [ ] Review all public evidence for sensitive data.
- [ ] Update the changelog and tag the Atlas v1 platform baseline.

## Confirmed Evidence Available

The latest supplied audit supports these statements:

- the host is a Dell Latitude E7250;
- Ubuntu Server 24.04.4 LTS and kernel 6.8.0-137-generic are installed;
- 16 GB of memory is installed;
- the host had 20 days of uptime at collection;
- the system SSD is the retained Samsung 256 GB device;
- SSH, Docker, WireGuard, Caddy, Prometheus, Node Exporter, Grafana, and Wazuh components were active;
- the primary LAN path at collection was Wi-Fi.

These observations do not replace the incomplete tests above.

## Evidence Record Template

Use one section per completed validation:

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
2. Validate local keyboard and display access.
3. Document network rollback.
4. Test wired networking without removing the known-good remote path.
5. Validate storage health and free space.
6. Measure temperatures and sustained-load behavior.
7. Validate power-management and reboot behavior.
8. Run extended reliability testing.
9. Reconcile documents, deferred work, cost, and final evidence.
10. Tag the completed Atlas v1 platform baseline.

Network and power-management changes can interrupt access. Perform them only when local recovery access is available.
