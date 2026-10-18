# Quick setup

**Start with one assistant reading your workspace, then try one useful task.**
Use an app, editor assistant or CLI you already have where it supports the needed
file access. A Windows and VS Code CLI walkthrough is included below.

## 1. Open the workspace

If you already have the folder, open it in your chosen tool. Otherwise, visit the
[repository page](https://github.com/neekode/agentic-workspace-template), choose
**Code > Download ZIP**, and extract it to a folder you want to work in. See
[GitHub's download guide](https://docs.github.com/en/repositories/working-with-files/using-files/downloading-source-code-archives).

If you already use Git, cloning is another route. For your own GitHub repository,
see [Make it yours](docs/workflow.md#make-it-yours).

Open the extracted or cloned folder containing AGENTS.md, this guide and examples.

## 2. Choose your assistant

Use a client that can read the workspace folder and edit files when you approve
changes. In an app or editor assistant, select that folder using its project or
folder controls. The [ChatGPT desktop quickstart](https://learn.chatgpt.com/docs/quickstart#setup-app-select-workspace)
shows one example; follow your chosen tool's instructions.

### Apps, CLIs and terminals

| Term              | What it means                                                                                                       |
| ----------------- | ------------------------------------------------------------------------------------------------------------------- |
| **Graphical app** | Software you use through windows, buttons and chat panels.                                                          |
| **CLI**           | **Command-line interface**: a text-based way to use software in a terminal. AI CLIs can take ordinary chat prompts. |
| **Terminal**      | A window or editor panel that hosts command-line programs.                                                          |

Both app and CLI clients can provide agents and file access; check the actual
tools and permissions available in yours.

**Before sharing private files:** review your provider's privacy controls and
the folder access you grant. Cloud assistants send working context to their
provider. See [privacy guidance](docs/tools.md#privacy-before-first-chat).

<details>
<summary>Windows and VS Code: set up a CLI</summary>

1. Install [VS Code](https://code.visualstudio.com/download) if you need an editor,
   then use **File > Open Folder** to open the workspace.
2. Choose **Terminal > New Terminal**, select PowerShell and run `Get-Location`.
   The location should be your workspace folder. See the
   [terminal introduction](https://code.visualstudio.com/docs/terminal/getting-started).
3. Choose one CLI from [tool setup](docs/tools.md#cli-setup), follow its installation
   and sign-in steps, then reopen the terminal. Check account requirements and
   costs; keep normal permission controls enabled.
4. Launch your chosen CLI from the workspace folder. For example, if you installed
   Codex, run:

```powershell
codex.cmd
```

Use the launch command in the tool notes if you chose another CLI. Paste commands
into the terminal; paste the prompts below into the assistant.

</details>

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
