# Quick setup

**Launch one AI CLI in your workspace, then try one useful task.**
This guide uses Windows, PowerShell and VS Code. Other editors and platforms
work too. No programming knowledge needed.

## 1. Open the workspace

Download and extract the [repository](https://github.com/neekode/agentic-workspace-template)
using **Code > Download ZIP**, or clone it if you use Git.
In [VS Code](https://code.visualstudio.com/download), choose **File > Open Folder**
and open the folder containing AGENTS.md and examples.

## 2. Set up and launch one CLI

### Apps, CLIs and terminals

A **CLI** (command-line interface) uses text commands instead of an app's buttons.
A **terminal** hosts it; **PowerShell** interprets your commands. AI CLIs also
accept ordinary chat prompts. [Why use one?](README.md#why-use-the-command-line)

Choose **Terminal > New Terminal**, select PowerShell from its dropdown and run:

```powershell
Get-Location
Get-ChildItem -Name
```

These show your folder and its files. Check for AGENTS.md and examples; if missing,
open the correct folder and a new terminal.

Choose **one CLI** from [tool setup](docs/tools.md#cli-setup), or use an installed
one. Check its account requirements and costs.

### Install Node.js and npm for npm-based tools

**Node.js** runs JavaScript programs; **npm** installs software bundles called
packages, including some AI CLIs. No JavaScript knowledge needed.

If your CLI's install command uses npm, check:

```powershell
node --version
npm.cmd --version
```

Missing a command? Install [Node.js LTS](https://nodejs.org/en/download)
(Long-Term Support), which includes npm. Reopen VS Code and repeat the checks;
both should print version numbers. Keep an existing Node setup if you have one.
Skip this for an already-working CLI or an installer that does not use npm.

### Install and launch the assistant

Use your CLI's install and launch commands in [tool setup](docs/tools.md#cli-setup).
Keep normal permission controls enabled. After installation, reopen the terminal
and check its folder. For Codex, check and launch with:

```powershell
codex.cmd --version
codex.cmd
```

Sign in when prompted. **Before sharing private files**, review
[privacy and folder access](docs/tools.md#privacy-before-first-chat): cloud
assistants send working context to their provider.

Type prompts inside the assistant; use another terminal for shell commands.

## 3. Verify workspace access

Paste this into the assistant:

> Read AGENTS.md and examples/README.md. Inspect only. Describe this workspace,
> the three example projects and the next step for one of them. Name the files
> you actually read. Do not edit files or install anything.

Check its file-reading activity where available. For future sessions, configure
[instruction loading](docs/tools.md#shared-instructions) for your chosen CLI.

## 4. Choose a project

- [Files](examples/files/README.md): inventory music or pictures and plan a clearer structure.
- [Magic](examples/magic/README.md): discover deck/catalog integrations before analysis.
- [Automation](examples/automation/README.md): research cross-ecosystem control.

Use its starting prompt. Complete one small task, review changes, explain one
decision and repeat one check yourself. Ask for `context` to resume later;
see the other [session requests](docs/workflow.md#session-requests).

## Optional: add another agent

Use the same CLI or another tool. Repeat the reading prompt, give writers separate
targets and keep Git operations sequential. See [working together](docs/workflow.md#working-together).
