# AI Workspace Starter Kit

A small, tool-agnostic template for organizing projects and working with multiple
AI assistants. Give your workspace any name. No always-on server is required.

**v0 baseline:** a lean starting point. Beginner walkthroughs and live integrations
still need acceptance; see the [work queue](now.md).

**Start with [QUICK-SETUP.md](QUICK-SETUP.md): get two different AI CLIs running
against the same workspace, then choose an example.**

## The workflow

Understand the need, research existing capabilities, reuse or configure a suitable
tool, and verify the result. Build something new only for a demonstrated gap.
MCPs, external integrations, application features, packages and scripts are central
to that discovery. See [tools and integrations](docs/tools.md).

Keep shared instructions in [AGENTS.md](AGENTS.md). Each project adds its own
purpose, constraints and current work. Use a short queue and maintain useful
results in place instead of accumulating session reports. The
[coaching prompt](docs/workflow.md#learn-by-checking) helps you explain a choice
and verify a result yourself.

## Examples

| Project                                          | What you can do                                                                    |
| ------------------------------------------------ | ---------------------------------------------------------------------------------- |
| [Files](examples/files/README.md)                | Organize music or pictures through an inventory, proposal and verified trial       |
| [Magic: The Gathering](examples/magic/README.md) | Retrieve a Moxfield deck, research cards through catalog tools and review the deck |
| [Automation](examples/automation/README.md)      | Research existing ways to coordinate devices across app ecosystems                 |

These are reusable scenarios from everyday work, with placeholders instead of
private household or account data. Connections are not preinstalled or live-tested.

[Workflow reference](docs/workflow.md) covers session requests, coordination and
adding your projects. [Tool notes](docs/tools.md) cover CLI setup and MCPs.
The optional [VS Code workspace](workspace.code-workspace) uses relative paths.

Bundled examples are tracked folders; real independent checkouts can live under
ignored `repos/`. Reproducible output can use ignored `cache/` when needed.
Neither folder is required. These instructions guide agents; your tools enforce
permissions. Cloud assistants still need appropriate access and internet.

Licensed under [MIT](LICENSE). Remaining release checks live in [now.md](now.md).
