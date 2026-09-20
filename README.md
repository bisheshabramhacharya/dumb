![banner](assets/banner.webp)

# dumb

ai responses are too verbose and hard to read. dumb fixes that.

it's a skill for coding agents with two jobs. first, it rewrites how the agent talks to you: next action first, numbered steps, no preamble, no recap, no "hope this helps!" garbage. second, it gives you a `/dumb` command. when a reply is too dense or full of jargon, type `/dumb` and it explains the same thing in plain language. every fact stays exactly the same, just said simpler.

## the two jobs

### job 1: say less, better (always on)

once it's on, every reply follows the shape:

- next action first. command, path, or snippet. prose after, if at all.
- numbered steps. one action per step, fewest steps that still work.
- one next action at the end, doable in under two minutes.
- lists capped at five. ranked.
- state restated every turn. no "keep in mind".
- real time estimates. "15 minutes if tests cover this, an afternoon if not."
- completed work shown concretely. "login works now, try `npm run dev`."
- errors stated flat. no "uh oh".
- no preamble, no recap, no closers.

### job 2: /dumb

your last message didn't land. `/dumb` re-explains it like to a smart friend. it never adds info and never answers something new. paths, numbers, filenames stay verbatim.

## the one rule

the reply says exactly what the source says. meaning preserved, facts verbatim, nothing invented. the rules rearrange the reply, they never change what it says.

## evals

`evals/` has the proof: dumb vs the two skills it replaced (`/bro` for plain speech, `/i-have-adhd` for the shape). inputs, outputs, comparison write-up.

## install

copy `SKILL.md` into your agent's skills dir. type `/dumb` when something needs simplifying, or keep it on for the whole session.
