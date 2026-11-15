# Dedicated Git Gemara Branch — Protection Contract

**Canonical reasoning branch:** `gemara`, separate from the source/product branch `main`.

The First Agent asks the owner to trigger `Bootstrap Git Gemara` in GitHub Actions, then verifies:
- `gemara` exists and contains `gemara/INDEX.md`, `gemara/PROTOCOL.md`, and `gemara/records/.gitkeep`;
- the branch has its own GitHub repository ruleset matching exactly `gemara`;
- deletion and force-push are blocked, updates require pull requests, and the agent has no bypass privilege;
- a test PR can add a reasoning record and merge under the configured review policy.

**Important:** GitHub's `restrict deletions` rule is an *administrative guard*, not mathematically irreversible storage. Repository administrators, privileged bypasses and repository deletion can defeat it. For genuine recovery, use independent backups/mirrors and protect their retention separately.

**Branch ruleset (owner manually applies in Settings → Rules → Rulesets):**
- Target: branch; include `gemara` exactly.
- Enforcement: Active.
- Restrict deletions: ON.
- Block force pushes: ON.
- Require a pull request before merging: ON; require at least one approving review where collaborators exist.
- Restrict bypass actors to none where supported.
- Consider signed commits and status checks once the workflow is verified.

For `main`, use a separate active ruleset with PR review, deletion/force-push restrictions, and required `validate` check after first green run.

If the hosting plan does not enforce rulesets on this public repository, **do not claim undelete**. Use a private repository/organization plan that supports the required protections or an external immutable backup.
