# Autonomous Company — Clean Starter Template

This repository is a **public, zero-tenant foundation** for starting an AI-operated company. It is not a clone of the private COS implementation and does not contain its internal history, deployments, provider bindings or credentials.

## Start
1. Use **Use this template** (or create a new private repository and copy this starter's files).
2. Read [FIRST_AGENT.md](FIRST_AGENT.md) with your first agent.
3. Create the Jira project and configure it using [company/JIRA_SETUP_GUIDE.md](company/JIRA_SETUP_GUIDE.md). Jira operations are manual until independently verified.
4. Record real, verified environment bindings in your own private environment, not in this public template.
5. Work from Git-native [Gemara](gemara/README.md), with reviewable commits and pull requests.

## Distribution
The pipeline validates the foundation and publishes a **source-only release artifact** from reviewed commits. It does **not** deploy infrastructure, provision Jira, install credentials, or assert that a company is operational.

## Security
No secrets, personal data, customer records, real provider IDs, tokens, or internal repository history belong here. See [SECURITY.md](SECURITY.md). Do not commit .env files. A passing scanner is not a guarantee that content is safe to publish.
