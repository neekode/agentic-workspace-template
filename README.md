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

## Starter session commands

Start with `context`, `status`, `discover`, `check`, `advance` and `trim`.
After the assistant reads AGENTS.md, try **`context for the Files example`**.
These are conversational shortcuts, not terminal commands. The
[reference](docs/workflow.md#session-requests) defines them and explains how to
adapt this boilerplate as your workflow grows.

## Why organize it this way?

**Governance** is your working agreement: how to research, get approval and check
results. Shared rules live in [AGENTS.md](AGENTS.md); projects add their purpose,
constraints and current work.

- **Contextualization:** relevant goals and decisions reduce repeated explanations.
- **Scope drift:** a short queue and clear limits keep work on the agreed goal.
- **Knowledge curation:** update useful notes, retire stale ones and promote
  recurring lessons into shared guidance.

The guidance evolves as you try, check and learn. Maintain results in place instead
of accumulating session reports. Use the [coaching prompt](docs/workflow.md#learn-by-checking)
to understand a choice and verify it yourself.

### Why use the command line?

A **CLI** (command-line interface) runs in a terminal and accepts chat prompts.
It lets you shape your editor and terminal layout, work in project folders and
combine assistants with local tools, MCPs and, where supported, scripts.
See [Codex's examples](https://learn.chatgpt.com/docs/codex/cli).

Apps can offer tools too; this workflow teaches direct control of your working
environment. Rules and project knowledge stay in readable files you can reuse
across compatible assistants. Each assistant must read them; chat histories stay
with their tools.

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

> **Privacy & analytics:** AI tools may collect usage data; cloud models receive
> prompts and selected context. See [privacy controls](docs/tools.md#privacy-before-first-chat)
> for training opt-outs and Codex's `config.toml` settings to disable optional
> analytics and diagnostic exports. Cloud processing still sends data off-device.

v0 · [MIT license](LICENSE) · [Template maintenance](now.md)
