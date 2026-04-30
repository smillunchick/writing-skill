# Audit Report Template

Use for `audit` mode and for final checks after drafting.

## Output shape

```markdown
## Verdict
[One-sentence bottom line.]

## Scores
| Dimension | Score | Notes |
|---|---:|---|
| Purpose fit | /5 | |
| Audience fit | /5 | |
| Structure/flow | /5 | |
| Specificity | /5 | |
| Voice consistency | /5 | |
| Persuasiveness | /5 | |
| Rhythm | /5 | |
| AI-slop risk | /5 | lower is better |

## What is working
- ...

## Highest-impact fixes
1. ...
2. ...
3. ...

## Span-level issues
| Span | Issue | Fix |
|---|---|---|
| “...” | ... | ... |

## Revision strategy
[Short plan.]

## Revised version
[Include if requested or clearly useful.]
```

## Severity labels

- **P0**: breaks trust, meaning, factuality, or required disclosure
- **P1**: major issue with structure, audience fit, or credibility
- **P2**: noticeable weakness in voice, specificity, rhythm, or persuasion
- **P3**: polish issue

## Audit dimensions

1. Purpose fit
2. Audience fit
3. Voice consistency
4. Structure and flow
5. Specificity
6. Persuasiveness
7. Rhythm
8. Concrete detail
9. AI-slop signals
10. Ending strength

## Audit guidance

- Be span-specific.
- Do not over-audit low-stakes writing.
- If the user only wants a verdict, keep it brief.
- If the text lacks human detail, flag the missing detail rather than inventing it.
