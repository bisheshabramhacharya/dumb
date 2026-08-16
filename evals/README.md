# dumb — eval log

Method: 8 dense source messages (the failure modes that motivated this skill — jargon, recap soup, fact-heavy instructions, ambiguous asks) routed through the merged skill, then checked against the quality contract: facts verbatim, nothing invented, meaning preserved, shape rules applied.

| Case | Source | Contract check | Result |
|------|--------|----------------|--------|
| s1 | Debug: failing test, paths, codes | 8/8 facts verbatim; cause→fix; matter-of-fact; no preamble | PASS |
| s2 | Ship instructions, 7 steps | All steps present; capped at 5 via do-now/later split | PASS |
| s3 | Jargon-heavy design review | 6/6 facts verbatim (4.1:1, 4.5:1, WCAG AA, 8pt, 768px); flattened, plain | PASS |
| s4 | Options question | Recommendation first; ranked 2–4; **miss: "3 people" reworded to "3-person team"** → fixed to verbatim | PASS after fix |
| s5 | Recap-heavy "I've done stuff" message | No recap-closer; wins visible; ends with concrete next action | PASS |
| s6 | PT-BR | Same language; flavor; cause+fix; facts verbatim | PASS |
| s7 | Ambiguous "make the button better" | One clarifying question — **miss: invented "~10 minute" estimate** → removed. Contract rule: never add what the source didn't state, even for shape | PASS after fix |
| s8 | DNS/API facts | 6/6 facts verbatim (IP, CNAME, URL, rate limit, key); numbered; next action | PASS |

## Misses → lessons (now enforced)

1. **Facts stay verbatim in wording, not just meaning.** "3 people" is not "3-person team" when the contract says verbatim. (s4)
2. **Time estimates only when grounded in real work.** Shape rule 6 never overrides the no-invention rule. (s7)

## Re-run

Pick any dense assistant message (or one of `evals/sN.in`), produce the skill-compliant reply, grep the output for every path/number/URL/name from the source, and check shape rules 1–10. Every miss is either an executor error (fix the reply) or a skill gap (fix SKILL.md).
