# Magic: deck research and analysis

## Purpose

Use a Moxfield deck and MTG catalog integrations to review a deck's plan, mana,
card access, interaction and constraints. Research existing capabilities before
browsing every card or writing a new deck-analysis script.

## Project inputs

- Deck: the user's chosen public Moxfield URL, not yet supplied.
- Format, theme and desired play experience: ask the user.
- Collection preference and budget: ask; a deck list is not ownership evidence.
- Review baseline: record the source and retrieval time once actually obtained.

## Reuse existing capabilities

[Moxfield](https://moxfield.com/) is the deck source;
[Scryfall](https://scryfall.com/docs/api) is a card-catalog research starting point.
Inspect available MCPs, plugins, native features and packages for deck retrieval,
card search, batch lookup and existing analysis. Catalog access alone does not
establish a deck-balance analysis capability.

One [community MCP candidate](https://github.com/cardosogguilherme/scryfall-moxfield-mcp)
reports Scryfall search/batch lookup and a Moxfield deck route. It is unvetted here:
inspect its current tool schemas, license, maintenance and access requirements,
then prove a read-only operation before recommending installation. It is not a
bundled or official Moxfield/Scryfall connection. Do not assume a public deck URL
provides a supported API; if retrieval is blocked, use a user-provided export
through the site's supported interface instead of bypassing access controls.

## Next

- [ ] Verify a suitable existing connection, retrieve the selected deck and
      resolve its cards through catalog tools. Separate active cards from sideboard
      and maybeboard, then produce a concise review tied to that exact list.

## Use the session commands

Use these inside the agent; shared meanings live in the
[workflow reference](../../docs/workflow.md#session-requests).

- `context examples/magic`: establish the chosen deck, format and goals.
- `discover examples/magic`: compare existing deck/catalog tools and access.
- `check examples/magic`: once connected with approval, verify read-only retrieval,
  the exact deck boards and card-data sources.
- `advance examples/magic`: complete the requested review using that verified list.
- `trim examples/magic`: propose consolidating notes or repeated findings.
- `status examples/magic`: report the reviewed list, result and next action.

## Start here

> Read this project's AGENTS.md and README. Discover existing tools for retrieving
> my chosen Moxfield deck and researching its cards in batches. Explain supported
> operations and gaps before suggesting installation or custom code. After a
> read-only connection is approved and proven, review the actual list against my
> goals. Separate measured counts, strategic judgments and proposed swaps.

**Useful result:** a traceable deck review and a small set of justified options.
Proposals do not change the adopted deck. No live integration has been tested here.

**Learner checkpoint:** verify one card claim against its catalog source and
explain which deck boards were analyzed. Explain why one proposed change fits
your goals, separating the source facts from strategic judgment.
