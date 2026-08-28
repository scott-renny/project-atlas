# Project Overview

## Purpose

Project Atlas documents the restoration and validation of a Dell Latitude E7250 as the Atlas v1 Ubuntu infrastructure server for the COC.

Atlas v1 is the current laptop platform. Atlas v2 is the later 2U rack replacement and is outside this repository phase.

## Objectives

- Extend the useful life of existing hardware.
- Maintain the installed 16 GB DDR3L memory configuration.
- Retain and validate the Samsung 256 GB M.2 2242 SATA SSD.
- Validate cooling and long-term reliability.
- Restore worn physical components in planned phases.
- Provide local maintenance access while using SSH routinely.
- Establish a stable wired-network path.
- Document decisions, evidence, tests, known limitations, and deferred work.

## Scope

This repository includes hardware assessment, memory and storage decisions, cooling improvements, physical repairs, local console hardware, wired-network hardware selection, host-platform validation, temperatures, stability testing, and sanitized evidence.

The repository may inventory services only when that evidence helps establish the host's current role. Detailed application configuration and the broader COC architecture are documented elsewhere.

This phase does not introduce Atlas v2 hardware requirements, new COC applications, Kubernetes expansion, or major service redesigns.

## Confirmed Baseline

The latest supplied audit identifies a Dell Latitude E7250 running Ubuntu Server 24.04.4 LTS with a 6.8.0-137-generic kernel, 16 GB of memory, and the retained Samsung system SSD. The host had 20 days of uptime at collection and was already operating as an infrastructure server.

The same audit showed that the primary LAN connection was Wi-Fi. Wired networking therefore remains an Atlas v1 platform-validation item and should be tested with a rollback path before any live network change.

## Storage Direction

Atlas will retain its Samsung 256 GB M.2 2242 SATA SSD. A purchased WD Blue SA510 1 TB M.2 2280 SATA SSD was physically incompatible and was not installed.

A future capacity upgrade will be considered only when actual requirements justify a compatible M.2 2242 SATA drive or separate external storage.

## Current Phase

Atlas is no longer in its initial assessment phase. It is in **platform validation and closeout**.

The phase checklist and evidence requirements are defined in [atlas-v1-completion.md](atlas-v1-completion.md). A checklist item is not complete merely because a component or service exists; completion requires current, sanitized evidence or an explicit deferral.

## Method

Every modification is planned, documented, tested, sanitized before publication, and verified before the next stage. Changes that could interrupt remote access—especially networking and power-management changes—require a rollback path and local access.
