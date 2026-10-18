# Quick setup

**Launch one AI CLI in your workspace, then try one useful task.**
This walkthrough uses Windows, PowerShell and VS Code to teach the terminal
workflow. You can use another editor or terminal and your CLI's platform guide.
You do not need to know programming to begin.

## 1. Open the workspace

If you already have the folder, use it. Otherwise, visit the
[repository page](https://github.com/neekode/agentic-workspace-template), choose
**Code > Download ZIP**, and extract it to a folder you want to work in. See
[GitHub's download guide](https://docs.github.com/en/repositories/working-with-files/using-files/downloading-source-code-archives).

If you already use Git, cloning is another route. For your own GitHub repository,
see [Make it yours](docs/workflow.md#make-it-yours).

Install [VS Code](https://code.visualstudio.com/download) if you need an editor.
Use **File > Open Folder** to open the extracted or cloned folder containing
AGENTS.md, this guide and examples.

## 2. Set up and launch one CLI

### Apps, CLIs and terminals

| Term              | What it means                                                                                                       |
| ----------------- | ------------------------------------------------------------------------------------------------------------------- |
| **Graphical app** | Software you use through windows, buttons and chat panels.                                                          |
| **CLI**           | **Command-line interface**: a text-based way to use software in a terminal. AI CLIs can take ordinary chat prompts. |
| **Terminal**      | A window or editor panel that hosts command-line programs.                                                          |

PowerShell is the **shell** that interprets the commands you type in the terminal.
Here, VS Code provides the editor and terminal; the CLI provides the assistant.
See [why use the command line](README.md#why-use-the-command-line).

Choose **Terminal > New Terminal** in VS Code and select PowerShell from the
terminal's dropdown. Run these commands one at a time:

```powershell
Get-Location
Get-ChildItem -Name
```

The first shows your current folder; the second lists its contents without
changing them. Check that the folder is your workspace and the list includes
AGENTS.md and examples. If not, reopen the correct folder and create a new
terminal. See the [terminal introduction](https://code.visualstudio.com/docs/terminal/getting-started).

Choose **one CLI** from [tool setup](docs/tools.md#cli-setup). If you already have
one installed, use it. Otherwise, follow its installation steps. Check account
requirements and costs, and keep normal permission controls enabled.

**Before sharing private files:** review your provider's privacy controls and
the folder access you grant. Cloud assistants send working context to their
provider. See [privacy guidance](docs/tools.md#privacy-before-first-chat).

After installation, reopen the terminal and check its folder again. Use the
version-check and launch commands for your chosen CLI in the tool notes. For
example, if you chose Codex:

```powershell
codex.cmd --version
codex.cmd
```

Follow your CLI's sign-in instructions when prompted. Type shell commands at the
PowerShell prompt; once the assistant is running, type ordinary requests into
its conversation. Open another terminal when you need to run shell commands
alongside it.

## 3. Verify workspace access

Paste this into the assistant:

> Read AGENTS.md and examples/README.md. Inspect only. Describe this workspace,
> the three example projects and the next step for one of them. Name the files
> you actually read. Do not edit files or install anything.

**Success:** the assistant can read the files and describe the workspace.
Inspect file-reading activity where available. You now have a working agent session.

For automatic instruction loading in later sessions, use the
[selected-tool guidance](docs/tools.md#shared-instructions).

## 4. Choose a project

- [Files](examples/files/README.md): inventory music or pictures and plan a clearer structure.
- [Magic](examples/magic/README.md): discover deck/catalog integrations before analysis.
- [Automation](examples/automation/README.md): research cross-ecosystem control.

**Useful first result:** complete one small task, explain one decision and repeat
one check yourself. Use the [coaching prompt](docs/workflow.md#learn-by-checking)
and the selected example's learner checkpoint.

Each README includes a starting prompt. Give the agent one named task and review
its result. See [working together](docs/workflow.md#working-together) when you need
another agent.

Review file changes in your editor. If you use Git, its history gives you local
checkpoints; VS Code's **Source Control** view helps review those changes.
Resume later by asking for `context` on your selected project. Other session
requests live in the [workflow reference](docs/workflow.md#session-requests).

## Optional: add another agent

A second session can review a finished result or work on a separate target. It
can use the same tool. Choose a different CLI when you want to compare tools or
need a capability your first tool lacks; check the added setup and usage costs.

Repeat the inspection prompt in each new session; conversations do not
automatically share context. Give simultaneous writers separate targets and keep
Git operations sequential. See [working together](docs/workflow.md#working-together).
