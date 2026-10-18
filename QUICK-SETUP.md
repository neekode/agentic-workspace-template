# Quick setup

**First milestone: two different AI CLIs reading the same workspace.** Then use
Files, Magic or Automation to try useful work. This ramp uses Windows and
VS Code; the files work with other editors. Other-platform walkthroughs remain
unverified. Cloud tools need internet, account access and possibly paid usage.

A terminal is a panel for launching programs. A CLI is a program you launch there.
An agent is an assistant session with access to permitted tools. A model is the
engine behind its responses; switching models inside one CLI does not create a
second CLI. Paste command blocks into the terminal and press Enter; paste quoted
prompts inside the agent.

## 1. Open the workspace

Install [Git](https://git-scm.com/downloads) and
[VS Code](https://code.visualstudio.com/download), then reopen VS Code.
If you already have this folder, use **File > Open Folder**. Otherwise copy the
repository's HTTPS URL, press **Ctrl+Shift+P**, choose **Git: Clone**, paste the URL
and open the resulting folder. Use GitHub's **Use this template** first, when
available, if you want your own repository; clone that new repository's URL.
Cloning the public source directly is fine for practice. Review the source before
trusting it.

Choose **Terminal > New Terminal**, select PowerShell and run:

```powershell
git --version
Get-Location
```

A version should appear, and the location should be your workspace folder.
Its file list should contain AGENTS.md, this guide and examples.

## 2. Install two CLIs

Choose two tools you can access from [tool setup](docs/tools.md#cli-setup).
Codex and Claude Code are a concrete pairing; Gemini is another option. Follow
the selected installation steps and browser sign-ins, then reopen the terminal.
Leave the normal permission controls enabled.

> [!IMPORTANT]
> **Review privacy before your first chat.** Cloud assistants send working context
> to their provider even when commands run locally. For Codex, follow
> [privacy setup](docs/tools.md#privacy-before-first-chat) to disable optional
> analytics, telemetry export and feedback submission, then check the separate
> account training controls. These settings preserve the agent's working context
> and tools; they do not guarantee zero retention. Review each chosen provider
> separately.

Create two terminals with the **+** button and rename them after the tools.
Both should start in the workspace root. Launch one CLI in each. For the pairing
above, use this in the Codex terminal:

```powershell
codex.cmd
```

And this in the Claude terminal:

```powershell
claude
```

If you chose another tool, use its launch command from the tool notes.

## 3. Verify shared context

Paste this into each assistant separately:

> Read AGENTS.md and examples/README.md. Inspect only. Describe this workspace,
> the three example projects and the next step for one of them. Name the files
> you actually read. Do not edit files or install anything.

**Success:** both CLIs can read the files and describe the same workspace.
Inspect file-reading activity where available. Their conversations remain separate;
shared files carry the project context. You now have a multi-CLI setup.

For automatic instruction loading in later sessions, ask the selected agent:

> Check your CLI's current project-instruction mechanism. If it needs an extra
> startup file to load AGENTS.md, create only that minimal project-local pointer.
> Keep the rules in AGENTS.md and report how I can verify it loaded.

The starter deliberately includes no loader files for unused CLIs.

## 4. Choose a project

- [Files](examples/files/README.md): inventory music or pictures and plan a clearer structure.
- [Magic](examples/magic/README.md): discover deck/catalog integrations before analysis.
- [Automation](examples/automation/README.md): research cross-ecosystem control.

**Second milestone:** complete one bounded task, explain one decision and repeat
one check yourself. Use the [coaching prompt](docs/workflow.md#learn-by-checking)
and the selected example's learner checkpoint.

Each README includes a starting prompt. Give one agent a named task, then have
the other review its finished result without editing. For simultaneous work, use
separate targets. Built-in delegation is optional; see [working together](docs/workflow.md#working-together).

Review file changes in VS Code's **Source Control** view before accepting them.
A local Git commit records a checkpoint; pushing or publishing is a separate
choice. Resume later by asking for `context` on your selected project.

If a command is missing, reopen the terminal and check its installation. For a
blocked npm-installed PowerShell launcher, use its `.cmd` form. If files are
missing, check the working folder and tool access. Other setup and instruction
loading details live in [tool notes](docs/tools.md).
