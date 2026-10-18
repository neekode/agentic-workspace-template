# Files: organize music or pictures

## Purpose

Make a computer's files easier to find and maintain. Choose a music or picture
folder, understand how it is used, and plan a clearer structure. This example
contains placeholders rather than a real person's filenames or library.

## Capture the starting point

| Collection | Possible goal                         | What to establish first                                 |
| ---------- | ------------------------------------- | ------------------------------------------------------- |
| Music      | Browse by artist and album            | Current tags, playlists and library paths               |
| Pictures   | Separate originals, edits and exports | Current folders, metadata and editor/catalog references |

Ask for the chosen folder, the user's preferred way to find things and what
already works. Research existing file-manager or library features before custom
scripts. Filenames and matching sizes alone do not prove duplicate content.

## Next

- [ ] Inventory one selected folder read-only, propose a naming/folder scheme
      with an exact before/after list, and choose a small trial for approval.

## Use the session commands

These are assistant requests; their shared meanings live in the
[workflow reference](../../docs/workflow.md#session-requests).

| Request                   | Use it here                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------- |
| `context examples/files`  | Establish the goal, chosen folder and known layout; ask for missing inputs.                  |
| `discover examples/files` | Find existing tools for browsing, tagging, cataloging or reorganizing this collection.       |
| `trim <chosen-folder>`    | Propose consolidation, renames or moves with exact targets; apply nothing.                   |
| `advance examples/files`  | After approval of the exact changes, apply one small batch using the selected existing tool. |
| `check <chosen-folder>`   | Verify the intended structure, file access and affected library/catalog references.          |
| `status examples/files`   | Summarize the result and one next action.                                                    |

Replace `<chosen-folder>` with the folder you selected. A proposal is not permission
to reorganize the entire computer. Keep originals, useful metadata and references
intact; review any deletion separately from simple moves.

## Start here

> Read this project's AGENTS.md and README. Context for examples/files: help me
> organize music or pictures. Ask which folder I want to work on and how I want
> to find things. Inspect only the selected scope, then use discover and trim
> to propose an approach before changing files.

**Useful result:** a maintainable structure and a verified small trial, with the
accepted result and next step kept here when the user requests recording.

**Learner checkpoint:** explain why the proposed structure fits how you find
music or pictures. After an approved trial, open one file and verify an affected
playlist or catalog reference yourself. Identify what evidence justifies any
proposed duplicate removal.
