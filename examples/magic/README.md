# Magic: deck research and analysis

## Purpose

Use a Moxfield deck to review its plan, mana, card access, interaction and
constraints. Research existing deck and MTG catalog capabilities before
browsing every card or writing a new deck-analysis script.

## Project inputs

- Deck: a user-selected public Moxfield URL or deck export.
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
inspect its current tool schemas, license, maintenance and access requirements
before recommending installation. If a connection is approved, test a read-only
operation. This is not a bundled or official Moxfield/Scryfall connection.

Start with tools already available. If direct retrieval is blocked, use a
user-provided export through the site's supported interface. Review the supplied
list while identifying useful catalog lookups or integration gaps; mark facts
that still need checking. Add a new MCP when its capabilities justify the setup.

## Next

- [ ] Obtain the selected deck through a supported connection or supplied export.
      Use available catalog data to check card facts, separate active cards from
      sideboard and maybeboard, and review the exact list against the user's goals.

## Use the session commands

Use these inside the agent; shared meanings live in the
[workflow reference](../../docs/workflow.md#session-requests).

- `context examples/magic`: establish the chosen deck, format and goals.
- `discover examples/magic`: compare existing deck/catalog tools and access.
- `check examples/magic`: verify the supplied or retrieved deck, its boards and
  card-data sources; test a new connection only within its approved scope.
- `advance examples/magic`: complete the requested review using that verified list.
- `trim examples/magic`: propose consolidating notes or repeated findings.
- `status examples/magic`: report the reviewed list, result and next action.

## Start here

> Read this project's AGENTS.md and README. Start with my chosen Moxfield URL or
> export and ask about my deck goals. Discover existing tools for deck retrieval
> and catalog research, using what is already available. Explain any setup that
> would help before installing or connecting tools. Review the actual list and
> separate checked facts, strategic judgments, proposed swaps and unresolved questions.

**Useful result:** a traceable deck review and a small set of justified options.
Proposals do not change the adopted deck. No live integration has been tested here.

**Learner checkpoint:** verify one card claim against its catalog source and
explain which deck boards were analyzed. Explain why one proposed change fits
your goals, separating the source facts from strategic judgment.
