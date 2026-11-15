# Manual Jira Foundation Setup

This is an operator guide, not an automated Jira deployment or a claim that a particular Jira edition supports every field/workflow operation.

1. Create a **new Jira project** for the new company. Record its name, project key and URL in the new company's private configuration.
2. Create an initial issue hierarchy supported by your Jira plan: company initiatives, deliverable epics, executable tasks and bounded research items. If issue types are unavailable, document the mapping to supported types.
3. Define statuses appropriate to your site: Backlog, Ready, In Progress, Blocked, In Review, Done. Configure transitions and permissions through the Jira administrator.
4. Define optional semantic fields, only where supported: professional owner, workstream, evidence link, Gemara reasoning link, dependency, acceptance evidence, blocked reason and next continuation.
5. Link related work using Jira's native relationships. Use real issue keys and verified URLs, never template IDs.
6. Create the first company-formation task and reference the Git Gemara entry.
7. Verify using a newly created test issue: creation, update, status transition, dependency link, field visibility, permissions and retrieval by a fresh agent.
8. Record limitations or unsupported operations explicitly. Never call the foundation deployed until independent readback succeeds.

**Security:** do not paste Jira API tokens into issues, Gemara, Git, logs or chat handoffs. Grant least-privilege access to agents and collaborators.
