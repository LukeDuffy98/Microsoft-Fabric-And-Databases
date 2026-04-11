# Operator Guide

This document is for the person wiring the lab into LabDesktops and validating the session before participants arrive.

## Delivery Model

This repository assumes:

1. One student-facing lab flow.
2. Shared Azure AI Foundry and Microsoft Fabric resources for the heavy platform components.
3. Optional lightweight per-student resources created inside each student resource group.

## Canonical Values

- `labId`: `fabric-foundry-lab`
- `readmePath`: `labs/fabric-foundry-lab/README.md`
- `instructionsTitle`: `Fabric + Foundry Lab Guide`

## Shared Resources Checklist

Provision these outside the student resource group unless there is a strong isolation reason:

1. Azure AI Foundry hub, project host, or equivalent shared entry point.
2. Shared model deployment sized for concurrent workshop usage.
3. Microsoft Fabric workspace and all required data artifacts.
4. Any shared documents, data files, or screenshots referenced in the lab.

## Per-Student Resources Checklist

This repo includes a starter Bicep template for per-student RG deployment.

Use per-student deployment only for resources that must be isolated, such as:

1. A lightweight storage account for uploads or temporary artifacts.
2. A student-specific resource needed for permissions or naming isolation.

Do not put large, slow, or quota-sensitive services into the per-student deployment path unless you have tested the startup time under realistic concurrency.

## Pre-Event Validation

1. Confirm the repo is publicly cloneable or otherwise reachable by the desktop container.
2. Confirm the rendered guide path exists exactly at `labs/fabric-foundry-lab/README.md`.
3. Confirm every image and document link in the student guide uses a relative path.
4. Confirm the lab guide does not duplicate credentials or guardrails already injected by LabDesktops.
5. Confirm the Template Spec version ID is current and points at the latest approved Bicep deployment.
6. Launch at least one student session end to end.
7. Time the full provisioning flow and record the observed startup duration.

## Facilitation Notes

1. Give students the generated LabDesktops URL with `studentId` and `labId` already included.
2. Keep the student guide stable during the event unless a correction is necessary.
3. If you update the guide during rehearsal, refresh the instructions pane to verify the change renders correctly.
4. Keep a short list of known issues and workarounds beside the delivery console.

## Post-Event Cleanup

Use the LabDesktops cleanup/reset workflow to remove expired student environments and any associated state.

If this repo evolves after the event, keep the `readmePath` stable unless you are also updating the LabDesktops catalog entry.