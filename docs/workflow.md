# Workflow reference

## Session requests

Type these inside an assistant conversation, with the project and desired outcome.
They are ordinary prompts, not installed shell programs or vendor slash commands.
Read the root [agreement](../AGENTS.md) and selected project instructions first.

| Request    | Meaning                                                                                            |
| ---------- | -------------------------------------------------------------------------------------------------- |
| `context`  | Inspect current guidance and work; explain the objective, progress and next action.                |
| `status`   | Give a brief snapshot and one next action.                                                         |
| `discover` | Research existing capabilities and propose a suitable approach. No installation.                   |
| `check`    | Review requirements and evidence using permitted read-only checks. Report findings.                |
| `advance`  | Complete the named, authorized slice, verify it and update its existing work home as useful.       |
| `trim`     | Propose removal, consolidation or cache relocation; apply only after approval of the reviewed set. |

`context`, `status`, `discover` and `check` are read-only. Normal requests such as
"update the docs" or "draft a commit message" work without additional vocabulary.
A task request does not grant unrelated Git, account, publication or device actions.

### Evolve your commands

When a request repeats, refine a command or add one with your assistant. Define
its outcome, whether it inspects or changes things, and a success check. Keep
shared meanings here and project variations in their AGENTS.md. Try a small task,
revise unclear instructions and retire unused commands.

## Learn by checking

A useful assignment names the target, desired outcome, limits and evidence of
success. When learning a new tool or task, try:

> Work through <project> with me. Explain why the chosen existing tool fits,
> point to the evidence behind one important decision, and give me one small
> step to perform or verify myself. Keep explanations brief and continue with
> already-authorized work.

At a natural stopping point, explain one choice in your own words and repeat one
check. If a result is unclear, ask what evidence would distinguish the options.
Use each example's learner checkpoint as self-assessment. Keep accepted results
in its existing home when recording is requested.

## Working together

An **agent** is an assistant session with access to tools; a **model** is the
engine behind its responses. Multiple agents can use the same app or CLI.
Multi-CLI means using different command-line programs.

Give each writer a named target and outcome. Start with one agent and review its
result. Optionally use a second session of the same tool, or another tool, to review
completed work. For parallel work, assign separate projects or nonoverlapping
files; one owner reviews shared changes afterwards.
Do not let agents mutate the same Git index or overlapping files concurrently.
Use sequential work or [Git worktrees](https://git-scm.com/docs/git-worktree)
for overlapping development, after choosing a committed starting point and branches.

A lead agent may delegate bounded work if your chosen tool supports it. Give
separate clients explicit assignments and the context each needs.
Use the project README or existing queue for durable progress and the next step.
Update that home when useful; do not create a report for every session. A newcomer
resumes by reading shared rules, local guidance and current work, then checking
fresh state rather than trusting a previous agent's claims.

## Add your projects

Add a folder for your own project with a short README naming its goal, current
work and next step. Its AGENTS.md links to the shared agreement and adds any
project-specific constraints. Keep an existing task list or product plan when
it already serves that purpose.

Bundled examples are ordinary tracked folders. Independent Git checkouts can live
under ignored `repos/<project>` and keep their own history, configuration and tasks.
Clone into an unused location; do not clone over existing work. Use **File > Add
Folder to Workspace** in VS Code if you want a combined view. Other editors work.

For a child at `repos/my-project`, its AGENTS.md should link to `../../AGENTS.md`,
name its purpose and current work home, and list domain constraints and real checks.
Configure automatic loading only for the chosen tool, as described in
[tool setup](tools.md#shared-instructions). Verify loading and update the shared
path if a checkout or worktree moves. Use an existing task home,
with Next / Backlog / Waiting where helpful and empty sections omitted.

Submodules are optional when you need shared remote URLs and pinned revisions.
Review each remote and committed state first; do not bulk-register dirty projects.
Keep editor-local state, credentials and private inventories out of published content.
Ignore rules do not remove files already staged or tracked.

## Make it yours

Use the examples that help and adapt the structure as your projects grow.
Keep original inputs and deliberate assets with their owners; use ignored
`cache/` for reproducible material when useful.
Cache is neither a backup nor deletion authority.

[GitHub templates](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
create independent repositories; later updates require review. If you want your
own GitHub repository, use **Use this template**, then clone that repository.
Record the source release if you need to review future template updates.
