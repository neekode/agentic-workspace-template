# AI Workspace Starter Kit

A small template for learning to work with AI assistants through the command
line: organize projects, keep useful context and connect existing tools.

**Start with [QUICK-SETUP.md](QUICK-SETUP.md): launch one AI CLI in your workspace,
then try an example.**

## The workflow

Understand the need, research existing capabilities, reuse or configure a suitable
tool, and verify the result. Build something new only for a demonstrated gap.
MCPs, external integrations, application features, packages and scripts are central
to that discovery. See [tools and integrations](docs/tools.md).

## Why organize it this way?

Governance is your working agreement with an assistant: how to research, what
needs approval, and how to check results. Shared rules live in [AGENTS.md](AGENTS.md);
each project keeps its own purpose, constraints and current work.

- **Contextualization** gives assistants relevant goals, facts and decisions,
  reducing repeated explanations between sessions.
- **Scope drift** is work wandering beyond the agreed goal. A short queue and
  explicit constraints help keep the next action focused.
- **Knowledge curation** keeps useful decisions and verified results current.
  Update existing notes, retire stale instructions, and move recurring lessons
  into shared guidance when other projects can benefit.

These habits create a feedback loop: try, check, learn and refine the guidance.
Git can track its evolution when you use it. The
[coaching prompt](docs/workflow.md#learn-by-checking) helps you understand a choice
and verify the result yourself.

### Why use the command line?

Web and desktop apps are one way to work with AI. A **CLI**, or command-line
interface, runs in a terminal and can still accept ordinary chat prompts.
Learning this route lets you choose your editor and terminal layout, work in
project folders, and combine assistants with local commands, existing tools and
MCP integrations. As needs grow, CLIs with scripting support can become part of
repeatable workflows; see [Codex's examples](https://learn.chatgpt.com/docs/codex/cli).

The aim is more control over your working environment and how tools fit together.
Graphical assistants can offer file access and integrations too; capabilities
depend on the tool and permissions. Here, your working agreement and project
knowledge stay in files you can inspect, edit and reuse across compatible tools.
Each assistant still needs to read them; chat history and app settings may stay
separate.

## Examples

| Project                                          | What you can do                                                                |
| ------------------------------------------------ | ------------------------------------------------------------------------------ |
| [Files](examples/files/README.md)                | Organize music or pictures through an inventory, proposal and verified trial   |
| [Magic: The Gathering](examples/magic/README.md) | Research and review a Moxfield deck using existing deck and card-catalog tools |
| [Automation](examples/automation/README.md)      | Research existing ways to coordinate devices across app ecosystems             |

Pick an example and start with its prompt.

[Workflow reference](docs/workflow.md) covers session requests, coordination and
adding your projects.
For a combined view in VS Code, open [workspace.code-workspace](workspace.code-workspace).

v0 · [MIT license](LICENSE) · [Template maintenance](now.md)
