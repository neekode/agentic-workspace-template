# Tools and integrations

## CLI setup

Use two tools you can access; check each provider's current account requirements
and costs. These are Windows PowerShell installation routes, not an installer
that the template runs. Official links also cover other platforms. Setup docs
were checked October 18, 2026; live walkthrough acceptance is still pending.

For npm routes, install [Node.js LTS](https://nodejs.org/en/download) if needed and
reopen your terminal. Check `node --version` and `npm.cmd --version` first.

| CLI         | Install                                 | Check / launch                        | Official guidance                                                                                                               |
| ----------- | --------------------------------------- | ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Codex       | `npm.cmd install -g @openai/codex`      | `codex.cmd --version` / `codex.cmd`   | [Setup](https://developers.openai.com/codex/cli/), [access](https://developers.openai.com/codex/auth/)                          |
| Claude Code | `winget install Anthropic.ClaudeCode`   | `claude --version` / `claude`         | [Setup](https://code.claude.com/docs/en/setup), [first session](https://code.claude.com/docs/en/quickstart)                     |
| Gemini CLI  | `npm.cmd install -g @google/gemini-cli` | `gemini.cmd --version` / `gemini.cmd` | [Setup](https://geminicli.com/docs/get-started/installation/), [access](https://geminicli.com/docs/get-started/authentication/) |

If WinGet is unavailable, use Claude's official native installer. Standalone
Codex installation is also documented upstream. Use the provider's troubleshooting
for failed downloads or sign-in; do not disable machine-wide protections or delete
dependencies blindly. The workspace itself has no runtime dependency.

## Privacy before first chat

Review privacy settings after signing in and before sharing private project data.
Each CLI and account has separate controls. Codex's default **user-level** file is
`%USERPROFILE%\.codex\config.toml` on Windows or `~/.codex/config.toml` elsewhere.
It affects other Codex workspaces too and stays outside this template.

### Edit the relevant settings carefully

1. Check `codex.cmd --version` and the current
   [configuration reference](https://learn.chatgpt.com/docs/config-file/config-reference).
   The version command identifies the CLI; it does not validate configuration.
   Open the existing file in your editor and keep it open through verification.
2. Find the existing definitions for analytics, feedback and otel. Update their
   current keys; add a missing section only once. TOML keys belong to the section
   above them until another header starts. Repeating a table or key can be invalid;
   see [TOML tables](https://toml.io/en/v1.0.0#table). Existing dotted or inline forms
   also count as definitions. Ask for help with the error and redacted relevant
   lines if you cannot identify where an edit belongs.
3. Review the change: only the intended settings should differ. Preserve unrelated
   values and use the editor's undo/history for the edits; do not replace the whole
   file or publish its contents. The block below shows the target settings.
4. Check syntax with a TOML-aware editor or parser if available, then restart the
   relevant Codex client when active work can safely pause. Check that it starts
   without configuration errors. If it fails, undo these edits and save. A syntax
   pass alone does not prove that the installed client supports every setting.

```toml
[analytics]
enabled = false

[feedback]
enabled = false

[otel]
exporter = "none"
trace_exporter = "none"
metrics_exporter = "none"
log_user_prompt = false
```

These settings disable optional analytics and diagnostic exports and block local
feedback submission. They preserve the model, tools, history and memory settings;
fewer exported diagnostics can make troubleshooting harder.
See [Codex telemetry and feedback controls](https://learn.chatgpt.com/docs/config-file/config-advanced#observability-and-telemetry).

Account controls need a separate check:

- **Personal ChatGPT sign-in:** turn off **Settings > Data controls > Improve the
  model for everyone**. This covers new ChatGPT conversations and Codex tasks.
  Check Codex's separate **Include environments** setting and turn it off if
  available; if it is absent, report it as unverified. Response feedback such as
  thumbs up/down can allow the associated conversation to be used for training
  despite the opt-out. See [ChatGPT data controls](https://help.openai.com/en/articles/7730893-data-controls-in-chatgpt).
- **API key:** review the key's organization and project
  [data-sharing settings](https://platform.openai.com/settings/organization/data-controls/sharing).
  Keep feedback, evaluation/fine-tuning data sharing, and input/output sharing
  disabled. API data is not used for model training by default, unless sharing is
  enabled. Other agent applications or SDKs have their own tracing controls.

Cloud model requests still transmit working context. Turning off analytics or
training does not eliminate service-side retention or connected-service logging;
review [API retention](https://developers.openai.com/api/docs/guides/your-data)
and each tool's data destinations separately. This template does not apply
account settings or configure other providers automatically. For another selected
CLI, review its own [Claude data-usage guidance](https://code.claude.com/docs/en/data-usage)
or [Gemini terms and privacy](https://geminicli.com/docs/resources/tos-privacy/)
for the account you use; the Codex settings above do not configure those tools.

## Shared instructions

AGENTS.md is the only instruction file supplied by default. Start each CLI with
an explicit request to read it, as shown in [quick setup](../QUICK-SETUP.md).
An agent cannot infer shared rules it has not loaded.

For later automatic loading, have the chosen agent verify its CLI's supported
mechanism and create only the needed project-local loader or configuration.
Claude and Gemini can use small imports; other tools may load AGENTS.md directly.
Keep one policy owner and verify actual file reads. Do not create files for tools
the user has not chosen. Launching inside a child also requires access to the
shared root guidance; a Markdown link is a reading request, not an automatic import.

Official behavior: [Codex](https://developers.openai.com/codex/guides/agents-md/),
[Claude](https://code.claude.com/docs/en/memory),
[Gemini](https://geminicli.com/docs/cli/gemini-md/).

## MCPs and external integrations

**Do not reinvent the wheel.** Discover existing applications, catalogs, packages,
plugins, CLIs, APIs and MCPs before choosing custom code or repetitive research.
Compare actual operations, compatibility, maintenance, permissions and cost.
Reuse good findings and refresh them when capabilities or requirements change.

MCP is a standard way for assistants to access tools and context from a server.
That server can be a local process or a remote service; local MCP use does not
require a dedicated always-on machine. A native app feature, CLI or API may be a
better fit for a particular job. See the official
[architecture](https://modelcontextprotocol.io/docs/learn/architecture) and
[local connection guide](https://modelcontextprotocol.io/docs/develop/connect-local-servers).

For a useful connection:

1. Define the job and inspect the actual exposed operations.
2. Review permissions and data destinations; get direction before installation
   or account connection. Share only nonsecret configuration and use the tool's
   supported credential storage.
3. Prove one permitted, representative operation and inspect the result.
4. Check startup and shutdown, including whether each CLI session starts another
   local process. Keep only connections with an actual consumer.

The [Magic example](../examples/magic/README.md) demonstrates catalog/deck-tool
research; [Automation](../examples/automation/README.md) demonstrates
choosing existing cross-vendor software. Neither ships a preconfigured connection.
