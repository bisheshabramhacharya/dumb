# dumb vs /bro vs /i-have-adhd — comparative eval

Same corpus, same contract checks, three skills. Facts checked by grep; shape checked against the rule sets of each skill.

## Coverage (what each skill can do)

| Job | /i-have-adhd | /bro | dumb |
|-----|--------------|------|------|
| Shape replies for an ADHD reader (persistent) | ✅ | ❌ only fires on /bro | ✅ |
| Re-explain last message in plain language | ❌ no simplification rules | ✅ | ✅ |
| Shape applied to re-explanations too | ❌ N/A | ❌ no shape rules | ✅ |

## Guarantees (what each skill's RULES demand, not what luck produced)

| Contract clause | /i-have-adhd | /bro | dumb |
|-----------------|--------------|------|------|
| Facts verbatim (paths, numbers, URLs unchanged) | ❌ no rule | ✅ rule 3 | ✅ |
| Nothing invented | ❌ no rule | ✅ rule 1 | ✅ |
| Meaning preserved | implicit only | implicit only | ✅ explicit, both jobs |
| Same language (PT-BR stays PT-BR) | ❌ unstated | ✅ rule 5 | ✅ |
| Lists capped at 5 | ✅ rule 9 | ❌ no rule | ✅ |

## Evidence from the corpus

- **adhd_s3 (jargon case, shaped by adhd alone):** "whitespace utilization is suboptimal", "type scale lacks hierarchical differentiation" — jargon survives. Shape fixes layout, not comprehension. The exact message that makes a reader type /bro.
- **bro_s5 (recap case, re-explained by bro alone):** one unnumbered 7-item list, no cap, no next action, no wins made visible. Plainer, but still a wall of text. The exact message an ADHD reader bounces off.
- **dumb s3/s5:** plain language AND capped numbered list AND next action. Both fixes in one reply.

## Where dumb is strictly stronger

1. **Shape on re-explanations** — a /dumb reply must be action-first, numbered, capped, no closer. /bro alone has none of these rules.
2. **Fact contract on persistent replies** — adhd alone has no fact-verbatim or no-invention rule; the eval caught an invented time estimate (s7) and a reworded fact (s4) that adhd's rules would not have flagged. dumb's contract makes both violations impossible-by-rule.
3. **Explicit meaning preservation** — neither original states it; both rely on the executor's good behavior.

## Verdict

dumb = /bro ∪ /i-have-adhd, plus the quality contract applied to both jobs. Equal on every axis where the originals have rules, stronger on the three above, and it covers both jobs instead of one. "Better" holds on coverage, on guarantees, and on the corpus.
