![banner](assets/banner.webp)

# dumb

A skill for coding agents that makes replies impossible to misunderstand.

It does two jobs. First, it reshapes how the agent writes: the next action comes first, steps are numbered, lists are capped at five, and there is no preamble, no recap, no "hope this helps". Second, it adds a `/dumb` command: when a reply didn't land, `/dumb` re-explains it in plain language, with every fact kept exactly as it was.

## Why

Most agent output is written to look complete, not to be acted on. Long preamble, hedged estimates, ten-item lists, wins buried in recaps. For anyone with ADHD, or anyone skimming between meetings, that shape is where work dies. dumb encodes the opposite shape as rules.

## The two jobs

### Job 1: ADHD-shaped output (persistent)

Once invoked, it applies to every reply for the rest of the session. The core rules:

- Lead with the next action. Command, path, or snippet first.
- Number multi-step tasks. One action per step, fewest steps that still work.
- End with one concrete next action, doable in under two minutes.
- Cap lists at five. Rank them.
- Restate state every turn ("step 3 of 5 done: schema updated, next: backfill the column").
- Give specific time estimates ("about 15 minutes if tests cover this, an afternoon if not").
- Make completed work visible, concretely ("login works with magic links now, try `npm run dev`").
- Matter-of-fact errors. Never "uh oh".
- No preamble, no recap, no closing pleasantries.

### Job 2: /dumb (say it simpler)

Type `/dumb` and the agent re-explains its last message in plain language, like to a smart friend over a beer. It never adds information and never answers a new question. Every path, number, and filename stays verbatim. Only the explanation around them gets simpler. Light bro flavor, same language as the original.

## The quality contract

Both jobs follow one contract, and it is non-negotiable: the reply says exactly what the source says. Meaning preserved, facts verbatim, nothing invented. The rules rearrange the reply. They never change what it says.

## Evals

`evals/` holds comparative runs: dumb against the two skills it merged (`/bro` for plain speech, `/i-have-adhd` for ADHD-shaped output). Inputs, outputs, and a comparison write-up, so the rules are argued from evidence, not taste.

## Install

Copy `SKILL.md` into your agent's skills directory. Invoke with `/dumb`, or ask the agent to keep it active for the session.
