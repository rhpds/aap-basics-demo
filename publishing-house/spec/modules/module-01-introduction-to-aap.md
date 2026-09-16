# Module 01 — Introduction to AAP

---

### Brief Overview

This module orients participants to Red Hat Ansible Automation Platform by walking through its core components and architecture. The presenter navigates a live Automation Controller instance, identifying the major UI areas and explaining how each component — inventory, credentials, projects, and the controller itself — fits into the overall platform. No prior AAP experience is assumed; the goal is to give beginners a concrete mental model before any hands-on authoring begins.

### Audience and Time

- **Audience:** Developers new to automation or evaluating AAP; beginner experience level
- **Prerequisites for this module:** None — this is the opening module
- **Duration:** 20 minutes

### Learning Objectives

- Identify the major components of Ansible Automation Platform (Automation Controller, inventory, credentials, projects, and job templates) and describe the role each plays in an automation workflow
- Navigate the Automation Controller web UI and locate the primary dashboard sections
- Explain at a high level how AAP fits into a developer's automation workflow, distinguishing it from running ad-hoc Ansible commands locally

### Lab Structure

| Section | Title | Duration |
|---------|-------|----------|
| 1 | AAP Architecture Overview | 7 min |
| 2 | Automation Controller UI Tour | 8 min |
| 3 | Exploring Pre-Configured Resources | 5 min |

### Detailed Steps

1. Open the Automation Controller URL in the browser and log in with the presenter credentials.
2. Point out the main dashboard — highlight the **Jobs**, **Hosts**, and **Recent Activity** summary tiles.
3. Explain the AAP architecture at a high level: the Controller orchestrates automation; inventories define target hosts; credentials store secrets; projects link to Git repositories containing playbooks.
4. Navigate to **Resources > Inventories** and open the pre-configured inventory. Show the host list and group structure.
5. Navigate to **Resources > Credentials** and open the pre-configured machine credential. Explain that credentials are stored encrypted and never exposed in logs.
6. Navigate to **Resources > Projects** and open the pre-configured Git-backed project. Show the SCM URL and the last sync timestamp.
7. Return to the dashboard. Summarize the relationship: a **Job Template** ties together an inventory, a credential, and a project (playbook) into a repeatable unit of automation.
8. Pause for brief questions (≤ 2 min) before transitioning to Module 02.

### Key Takeaways

- AAP centralises automation with role-based access control, audit logging, and secret management — capabilities absent from a plain Ansible CLI setup
- The Automation Controller UI provides a single pane of glass for all automation activity
- Inventories, credentials, and projects are reusable building blocks composed by job templates
- A shared, pre-configured presenter environment means participants can follow along in the UI without any local setup

### Infrastructure Notes

- A pre-deployed AAP instance with Automation Controller must be running and accessible via browser before the session starts
- The environment includes a pre-configured inventory (sample hosts), a machine credential, and a Git-backed project pointing to a starter playbook repository — no live setup is performed during this module
- Infrastructure details (cloud provider, AAP version, cluster type) are TBD and will be confirmed in the infrastructure phase
