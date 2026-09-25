# Project Overview and Methodology

## Project identification

- **Project:** Cloud Security Operations Blueprint: Building a Governed Cloud Environment
- **Organization:** Peachtree Logistics Group (PLG), a fictional regional logistics company
- **Workload:** Proposed migration of PLG's dispatch and delivery platform to AWS
- **Artifact status:** Reference design and simulated case study; no production deployment or operating effectiveness is claimed
- **Prepared by:** Tommy Marshall

## Purpose

PLG needs a dependable dispatch platform for employees and independent couriers. Moving the platform to AWS creates decisions about access, sensitive delivery information, monitoring, incident response, and recovery. This project documents those decisions and shows how PLG would govern the resulting environment.

The central trace is:

**Business requirement → risk → architecture decision → control → owner → test → evidence → monitoring.**

## Method

1. Define the business process, stakeholders, scope, and assumptions.
2. Inventory the proposed components and classify the data they handle.
3. Map users, interfaces, data flows, and trust boundaries.
4. Assess risks using a stated scoring method.
5. Design AWS account, identity, network, application, data, and monitoring controls.
6. Assign ownership under the AWS shared responsibility model.
7. Define implementation order, tests, evidence, exceptions, and measures.
8. Review the package for consistency and communicate residual risk.

NIST Cybersecurity Framework (CSF) 2.0 organizes the desired outcomes. The AWS Well-Architected Security Pillar and AWS Security Reference Architecture inform design choices. Framework references guide this fictional design; they do not certify compliance.

## How to read this repository

Start with [business context](01-business-context-and-requirements.md), [scope](02-scope-assumptions-and-stakeholders.md), [inventory](03-system-and-data-inventory.md), and [data flows](04-data-flows-and-trust-boundaries.md). Then read the [risk assessment](05-cloud-risk-assessment.md) alongside the design in documents 07–13. Documents 14–18 describe implementation, assurance, reporting, residual risk, and executive conclusions.

Control identifiers use `CLD-01` through `CLD-12`; risk identifiers use `R-01` through `R-08`. The detailed mappings belong in `controls/cloud-control-matrix.md` and `controls/framework-crosswalk.md`.

## Evidence rule

A design, configuration proposal, template, or simulated record is **not proof that a control operates in AWS**. Actual implementation claims would require dated configuration exports, approved records, test results, and review by the designated owner.
