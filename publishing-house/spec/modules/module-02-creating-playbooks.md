# Module 02 — Creating Playbooks

---

### Brief Overview

This module demonstrates how to author and execute a simple Ansible playbook directly within the AAP environment. The presenter walks through playbook structure — plays, tasks, and modules — then creates a minimal playbook in the Git-backed project and triggers a run from the Automation Controller. Participants observe real-time output in the job detail view, making the connection between YAML authoring and live infrastructure changes tangible.

### Audience and Time

- **Audience:** Developers new to automation or evaluating AAP; beginner experience level
- **Prerequisites for this module:** Module 01 (Introduction to AAP) — participants should understand what a project and inventory are before this module begins
- **Duration:** 20 minutes

### Learning Objectives

- Describe the structure of an Ansible playbook: plays, tasks, and built-in modules
- Author a minimal playbook that targets the pre-configured inventory and executes at least one task (e.g., a file or command module)
- Trigger a playbook run from the Automation Controller and interpret the real-time job output, identifying successful and failed tasks

### Lab Structure

| Section | Title | Duration |
|---------|-------|----------|
| 1 | Playbook Anatomy | 5 min |
| 2 | Write a Minimal Playbook | 10 min |
| 3 | Execute and Observe Output | 5 min |

### Detailed Steps

1. Return to **Resources > Projects** and open the pre-configured project. Explain that playbooks live in the linked Git repository.
2. Open the repository in a browser or editor accessible to the presenter. Show the existing directory structure (e.g., `playbooks/`, `inventory/`).
3. Explain playbook anatomy on screen:
   - A **play** targets a set of hosts from the inventory
   - A **task** calls an Ansible **module** to perform one unit of work
   - YAML indentation defines the structure
4. Create a new file `playbooks/demo.yml` with a minimal play:
   - `hosts:` set to the inventory group shown in Module 01
   - One task using `ansible.builtin.debug` or `ansible.builtin.command` to produce visible output
   - A `name:` field on both the play and the task so output is readable
5. Commit and push the file to the repository (or demonstrate with a pre-staged commit if live Git operations are outside scope).
6. Back in the Automation Controller, navigate to **Resources > Projects** and click **Sync** on the project to pull the latest commit.
7. Navigate to **Resources > Job Templates** and select (or create) a job template that points to this project and the `playbooks/demo.yml` playbook path.
8. Click **Launch**. The job detail view opens automatically.
9. Walk through the real-time output: point out the play header, the task name, the `ok` or `changed` status, and the final recap line showing host counts.
10. Pause for brief questions (≤ 2 min) before transitioning to Module 03.

### Key Takeaways

- Ansible playbooks are human-readable YAML files that describe automation tasks in plain language
- The `hosts` key links a play to an inventory group, keeping playbooks decoupled from specific IP addresses or hostnames
- AAP's real-time job output (with colour-coded status per task) makes it far easier to diagnose automation runs than tailing a log file manually
- Syncing a project pulls the latest Git commit — all playbook changes flow through version control

### Infrastructure Notes

- The pre-configured Git-backed project must be writable by the presenter (or a pre-staged commit with `playbooks/demo.yml` must already be on the default branch) so the sync step succeeds within the module's time budget
- If live Git editing is not feasible, the presenter may use a pre-prepared branch and toggle it in the project SCM settings before the session
- No per-participant provisioning is required; this is a single shared presenter environment
- Infrastructure details (cloud provider, AAP version, cluster type) are TBD and will be confirmed in the infrastructure phase
