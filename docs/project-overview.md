# Project Overview

## Purpose

Project Atlas documents the restoration and validation of a Dell Latitude E7250 as the Atlas v1 Ubuntu infrastructure server for the COC.

Atlas v1 is the current laptop platform. Atlas v2 is the later 2U rack replacement and is outside this repository phase.

## Objectives

- Extend the useful life of existing hardware.
- Maintain the installed 16 GB DDR3L memory configuration.
- Retain and validate the Samsung 256 GB M.2 2242 SATA SSD.
- Document the completed physical restoration.
- Validate cooling, networking, power behavior, local maintenance access, and long-term reliability.
- Document decisions, evidence, tests, known limitations, and deferred work.

## Scope

This repository includes hardware assessment, completed physical upgrades, memory and storage decisions, cooling improvements, local console hardware, Wi-Fi network operation, host-platform validation, temperatures, stability testing, and sanitized evidence.

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

## Current Phase

Atlas is in **platform validation and closeout**. The remaining work is evidence collection and operational validation, not further physical upgrading, cleaning, or maintenance.

The phase checklist and evidence requirements are defined in [atlas-v1-completion.md](atlas-v1-completion.md). A checklist item is complete only when supported by the audit, owner confirmation of physical installation, or sanitized validation evidence.

## Method

Every modification is documented, tested, sanitized before publication, and verified. Changes that could interrupt remote access—especially networking and power-management changes—require a rollback path and local access.
