# Module 03 — Job Templates

---

### Brief Overview

This module shows how job templates in AAP package a playbook, inventory, and credential set into a repeatable, shareable automation unit. The presenter creates a new job template from scratch, configures its core parameters, and launches it — demonstrating how teams can standardise automation runs without requiring every operator to know the underlying playbook details. This is the capstone module, tying together the components introduced in Modules 01 and 02.

### Audience and Time

- **Audience:** Developers new to automation or evaluating AAP; beginner experience level
- **Prerequisites for this module:** Module 01 (Introduction to AAP) and Module 02 (Creating Playbooks) — participants should be familiar with the Automation Controller UI, inventories, credentials, projects, and basic playbook structure
- **Duration:** 20 minutes

### Learning Objectives

- Explain the purpose of a job template and how it ties together a playbook, inventory, and credential into a reusable automation unit
- Create a job template in the Automation Controller UI by selecting a project, playbook, inventory, and credential
- Launch a job template and interpret the resulting job output, confirming that the correct playbook ran against the correct hosts

### Lab Structure

| Section | Title | Duration |
|---------|-------|----------|
| 1 | What Is a Job Template? | 5 min |
| 2 | Create a Job Template | 10 min |
| 3 | Launch and Review Results | 5 min |

### Detailed Steps

1. Navigate to **Resources > Job Templates** in the Automation Controller UI.
2. Explain what participants see: any existing templates in the list represent pre-packaged automation units ready to launch with a single click.
3. Click **Add** to open the new job template form. Walk through each required field as it is filled in:
   - **Name:** give the template a descriptive name (e.g., `Demo - Hello World`)
   - **Job Type:** leave as `Run`
   - **Inventory:** select the pre-configured inventory from Module 01
   - **Project:** select the Git-backed project synced in Module 02
   - **Playbook:** choose `playbooks/demo.yml` from the dropdown (populated from the project)
   - **Credentials:** select the pre-configured machine credential from Module 01
4. Expand the **Options** section and briefly highlight available toggles (e.g., privilege escalation, verbosity) — explain them but leave defaults for this demo.
5. Click **Save**. The template detail page opens.
6. Click **Launch** from the template detail page.
7. The job detail view opens. Walk through the output:
   - Confirm the correct inventory hosts appear in the play header
   - Point out the task names and status badges (`ok`, `changed`, `failed`)
   - Read the final **PLAY RECAP** line and explain what the host counts mean
8. Return to **Resources > Job Templates** and show that the template is now listed and can be re-launched by any authorised user without any playbook knowledge.
9. Summarise the full demo arc: components (Module 01) → playbook authoring (Module 02) → standardised, repeatable execution via job templates (Module 03).
10. Open the floor for final questions.

### Key Takeaways

- Job templates are the primary mechanism through which AAP makes automation repeatable and accessible to non-experts
- Separating the playbook (in Git) from the execution parameters (in the job template) enforces good separation of concerns and enables RBAC — different teams can launch templates without seeing the underlying YAML
- The Automation Controller records every job run with full output, providing an audit trail out of the box
- A job template created once can be re-launched, scheduled, or embedded in a workflow — setting the stage for more advanced AAP features beyond this demo

### Infrastructure Notes

- The pre-configured inventory, credential, and project must all be in place before this module begins (established in Module 01 and used in Module 02); no additional infrastructure setup is required for Module 03
- If the job template from Module 02's execution step already exists, the presenter may choose to demonstrate editing an existing template rather than creating a new one — either approach covers the learning objective
- Infrastructure details (cloud provider, AAP version, cluster type) are TBD and will be confirmed in the infrastructure phase
