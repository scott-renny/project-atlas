# Project Overview

## Purpose

Project Atlas documents the restoration and validation of a Dell Latitude E7250 as the Atlas v1 Ubuntu infrastructure server for the COC.

Atlas v1 is the current laptop platform. Atlas v2 is the later 2U rack replacement and is outside this repository phase.

## Objectives

- Extend the useful life of existing hardware.
- Maintain the installed 16 GB DDR3L memory configuration.
- Retain and validate the Samsung 256 GB M.2 2242 SATA SSD.
- Document the completed physical restoration.
- Validate cooling, networking, power behavior, local maintenance access, unattended recovery, and long-term reliability.
- Document decisions, evidence, tests, known limitations, and deferred work.

## Scope

This repository includes hardware assessment, completed physical upgrades, memory and storage decisions, cooling improvements, local console hardware, Wi-Fi network operation, host-platform validation, power resilience, temperatures, stability testing, and sanitized evidence.

The repository may inventory services only when that evidence helps establish the host's current role. Detailed application configuration and the broader COC architecture are documented elsewhere.

This phase does not introduce Atlas v2 hardware requirements, new COC applications, Kubernetes expansion, or major service redesigns.

## Confirmed Baseline

The supplied system audit identifies a Dell Latitude E7250 running Ubuntu Server 24.04.4 LTS with a 6.8.0-137-generic kernel, 16 GB of memory, and the retained Samsung system SSD. The host had 20 days of uptime at collection and was already operating as an infrastructure server.

The audit showed that the primary LAN connection was Wi-Fi. No external wired-network adapter is installed, and one will not be added in Atlas v1. Wi-Fi is the intentional network path for this version; the lack of wired networking is an accepted Atlas v1 limitation.

## Physical Restoration Status

The owner confirms that the memory, cooling stand, local keyboard, external display path, replacement battery, and replacement bottom cover are installed. All cleaning and physical maintenance are also complete. Physical restoration and maintenance are therefore complete.

This confirmation records installation, not unobserved technical test results. Component models, dates, costs, photographs, and validation evidence should be added where they are not yet recorded.

## Storage Direction

Atlas retains its Samsung 256 GB M.2 2242 SATA SSD. A purchased WD Blue SA510 1 TB M.2 2280 SATA SSD was physically incompatible and was not installed.

A future capacity upgrade will be considered only when actual requirements justify a compatible M.2 2242 SATA drive or separate external storage.

## Unattended Operation and Recovery

A September 7, 2026 resilience milestone was completed before the project owner left home for approximately three weeks to support a new site and train managers and team leads. That absence created a practical infrastructure requirement: Atlas needed to keep operating without physical intervention and recover cleanly from routine reboots and power interruptions.

The validation confirmed:

- BIOS `Wake on AC` powers Atlas back on automatically after AC is restored;
- a clean reboot returns the host to an administrable state;
- the replacement battery can provide short-duration backup power;
- a systemd watchdog checks AC and battery state every minute and initiates a clean shutdown at 35% or below when AC is absent;
- core host services and private remote-access components return automatically after reboot;
- production Docker containers recover via `unless-stopped` restart policies;
- Pi-hole returns healthy after reboot;
- the host reaches a clean `running` systemd state with zero failed units;
- Ubuntu security maintenance is automated while potentially disruptive updates and reboots remain deliberate.

The resilience milestone deliberately reused existing hardware and native platform capabilities rather than adding unnecessary complexity. This reflects the project's simplicity-first approach: use what already works, configure it correctly, integrate it, and only build something new when a real gap remains.

See [evidence/atlas-v1-resilience-validation-2026-09-07.md](evidence/atlas-v1-resilience-validation-2026-09-07.md).

## Current Phase

Atlas is in **platform validation and closeout**. Physical restoration is complete, and the pre-travel unattended-operation/power-recovery milestone is complete. Remaining work is limited to evidence and operational checks that have not yet been proven, including SSD health, thermal baselines, selected local-console and lid/suspend behavior, and extended reliability.

The phase checklist and evidence requirements are defined in [atlas-v1-completion.md](atlas-v1-completion.md). A checklist item is complete only when supported by the audit, owner confirmation of physical installation, or sanitized validation evidence.

## Method

Every modification is documented, tested, sanitized before publication, and verified. Changes that could interrupt remote access—especially networking and power-management changes—require a rollback path and local access.

The operational principle established during the resilience milestone is: **recovery is automatic, security maintenance is automatic where safe, and potentially disruptive change is deliberate.**
