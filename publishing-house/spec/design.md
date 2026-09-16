# AAP Basics Demo

## Overview

This demo showcases the core capabilities of Red Hat Ansible Automation Platform for developers new to automation. Participants will see AAP in action through a guided presenter-led session covering the platform's key components, playbook authoring, and job template configuration. By the end, developers will have a concrete picture of how AAP accelerates automation workflows.

Participants will observe AAP's Automation Controller UI, watch the presenter create and execute a simple playbook, and see how job templates standardize and schedule automation runs.

## Target Audience

- **Role:** Developers new to automation or evaluating AAP
- **Experience level:** Beginner
- **What they already know:** Basic familiarity with the command line or scripting; no prior Ansible or AAP experience assumed
- **What they don't know:** AAP architecture, Ansible playbook syntax, job templates, and how AAP fits into a development workflow

## Prerequisites

- None beyond basic familiarity with the command line
- No automated validation — trust-based prerequisite

## Learning Objectives

1. Explore AAP's core components and architecture
2. Create and run playbooks
3. Configure job templates

## Content Type

Demo (presenter-led)

## Products & Technologies

- Red Hat Ansible Automation Platform

## Module Map

| Module | Title | Duration |
|--------|-------|----------|
| 1 | Introduction to AAP | 20 min |
| 2 | Creating Playbooks | 20 min |
| 3 | Job Templates | 20 min |
| — | **Total demo content** | **60 min** |
| — | Intro / framing | ~5 min |
| — | **Total session** | **~65 min** |

## Difficulty Level

Beginner

## Environment

**Learner view:** A pre-deployed Red Hat Ansible Automation Platform instance is running and accessible. The Automation Controller UI is open in the browser. Sample inventory, credentials, and a starter project are pre-configured so the presenter can proceed directly to playbook creation without setup overhead.

**Automation needed:** Yes — an AAP instance with Automation Controller must be provisioned, with a pre-configured inventory, credential store, and Git-backed project. No per-student provisioning — this is a single shared presenter environment.

## Infrastructure Requirements

- **Cloud provider:** CNV
- **Cluster type:** N/A (RHEL VM-based, not OCP)
- **OCP version:** N/A
- **Topology:** Shared-cluster (single presenter environment)
- **Sizing:** 1 AAP Automation Controller (8 vCPU, 32GB RAM); 2 RHEL managed nodes (2 vCPU, 8GB RAM each)
- **Automation approach:** Ansible
- **AI/MaaS:** None
- **External services:** registry.redhat.io, github.com, cdn.redhat.com
- **AAP version:** 2.5
- **Non-GA products:** None (all products are GA)
