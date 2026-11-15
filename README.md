# Autonomous Company — Portable Foundation Template

A **public, clean-room starter** for establishing a persistent AI-operated company. No internal COS/IAA reasoning history, deployment records, provider bindings or credentials are included.

## Installation in a new company
1. Click **Use this template** and create your own repository (prefer private until configured).
2. Read [FIRST_AGENT.md](FIRST_AGENT.md) and launch the First Agent using [its launcher](prompt-system/launchers/FIRST_AGENT.md).
3. The First Agent guides the owner through [manual Jira provisioning](company/JIRA_SETUP_GUIDE.md) and verifies real project/field/workflow state.
4. In **Actions → Bootstrap Git Gemara → Run workflow**, run from `main`. The workflow creates an independent `gemara` branch, preserving its history on future runs.
5. **Before claiming protected:** configure the `gemara` branch deletion/force-push/PR ruleset described in [GEMARA_BRANCH_POLICY.md](company/GEMARA_BRANCH_POLICY.md). GitHub ruleset settings are not configured by the workflow.
6. Use the [portable prompt runtime](prompt-system/README.md) to activate Lead, Orchestrator, Prompt Master and Product Presenter as needed.
7. Confirm cold-start: a fresh agent can read Jira + the dedicated Git Gemara branch and continue without the original chat.

## Authority and architecture
- `main`: product, prompts, configuration templates and validation pipeline.
- `gemara`: **company-specific reasoning**, records, objections, correction lineage, WHY/WHY-NOT. Read/write on this branch, not on `main`.
- Jira: operational commitments, dependencies, workflow and ownership.
- Owner: intent and external authority.
- Agents: replaceable intelligence with stable professions.

The runtime is a **portable adaptation** of the COS philosophy, not a verbatim copy of COS V3.2 or the Confluence-backed Gemara vNext product.

## Distribution pipeline
[Validate and package](.github/workflows/validate-and-package.yml) checks source structure and creates a source artifact; [Bootstrap Git Gemara](.github/workflows/bootstrap-gemara.yml) creates the separate branch on demand. Neither provisions Jira nor applies GitHub repository rulesets.

## Security
Public source and Git history are visible to everyone. Review [SECURITY.md](SECURITY.md), enable secret scanning/push protection, and enforce rulesets on `main` and `gemara` in repository settings.
