# Loomi Connect error handling

Gives an assistant a fixed way to respond when Loomi Connect fails, and a checklist of questions to settle before building, so work is not repeated. It covers:

- Timeouts, access errors and rate limits.
- Writes that are rejected or whose saved state is unclear.
- EQL cost limits.
- Wrong or empty numbers.
- Claims that have no query behind them.

| | |
|---|---|
| **Products** | Engagement, Discovery, Data Hub |
| **Access** | Read-only |
| **Loomi Connect tools** | `list_cloud_organizations`, `list_projects`, `search_tools`, `call_tool`, `estimate_eql_cost`, and read tools for state checks |
| **Tested with** | Claude Desktop app, on a live production Bloomreach Engagement project. Not tested in an OpenAI client. Tested by Konstantin Protivenskiy |
| **Maintainer** | Konstantin-Protivenskiy-CRM |

## Example prompts

- "My create_scenario call timed out. What should I do before retrying?"
- "I'm about to build a lifecycle scenario. What do we need to settle first?"
- "This query returned zero events but I know there are some."
- "Loomi Connect says access denied. What now?"

## What is inside

- `SKILL.md`: the steps, the five rules and the safety statement.
- `references/error-playbook.md`: 28 known errors with causes and fixes, each marked as documented or observed.
- `references/gap-checklist.md`: questions to settle before a build or analysis.
- `references/working-agreements.md`: a brief template and habits that reduce rework.

## Notes and limitations

- The skill never changes anything itself. Retries and test writes are recommended, and the user asks the skill or tool that made the change to carry them out.
- Entries marked "observed" in the playbook come from hands-on use and can change as the tools change.
- `loomi-connect-feedback` reports a Loomi Connect tool problem to the team. This skill is about recovering safely and avoiding rework, and it points to that skill for errors it does not know.
- `engagement-number-reconciliation` explains why two numbers disagree. This skill covers wrong or empty results as one case among many.
