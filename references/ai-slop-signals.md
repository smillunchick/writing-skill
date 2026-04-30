# AI-Slop and Human-Specificity Signals

Use this reference during `audit`, `humanize`, `revise`, and final tournament passes.

## Common AI-slop signals

Watch for patterns, not isolated words.

### Generic framing
- “In today’s fast-paced world”
- “It is important to note”
- “Now more than ever”
- broad universal openings before the actual point

### Overused connective tissue
- moreover
- furthermore
- additionally
- in conclusion
- ultimately
- notably
- whether you’re X or Y

### LLM-signature vocabulary
- delve
- tapestry
- landscape
- robust
- seamless
- elevate
- unlock
- foster
- underscore
- pivotal
- crucial
- intricate
- palpable
- realm
- testament
- leverage

### Structural tells
- too many three-part lists
- “not only X but also Y”
- perfect paragraph symmetry
- every paragraph ends in a neat mini-summary
- generic inspirational close
- “helpful assistant” tone

### Linguistic density
- abstract noun stacks
- nominalizations where verbs would be clearer
- overloaded participial clauses
- “implementation of / optimization of / facilitation of” phrasing

### Weak human signal
- no concrete examples
- no situated detail
- no specific reader context
- no real constraint or tradeoff
- emotions are explained instead of shown
- point of view is excessively neutral

## Human-specificity improvements

Prefer:
- concrete nouns and verbs
- real examples, numbers, scenes, constraints
- genuine point of view
- uneven but purposeful rhythm
- quieter endings
- reader-specific context
- admitted uncertainty where honest
- specific tradeoffs instead of generic benefits

## Missing-detail flags

If the text cannot be made genuinely human because it lacks source material, say so and ask for one or more of:

- a real example
- a concrete moment
- the actual audience
- what the writer really thinks
- a number, name, place, or constraint
- what should not be said
- what prompted the writing

## Humanization prompt

```text
Revise this for human specificity, not detector evasion.

Preserve the meaning. Cut generic setup. Replace abstractions with concrete details where the source supports it. Remove obvious AI-signature phrasing. Vary rhythm. Keep useful roughness. Do not add fake anecdotes, fake emotion, fake citations, or fake personal experience.

First identify the most AI-sounding spans. Then rewrite.
```
