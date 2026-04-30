---
name: writing
description: >
  Use when drafting, revising, humanizing, auditing, polishing, or developing
  voice-sensitive prose. Covers blank-page writing, notes-to-draft, multi-variant
  draft tournaments, best-parts synthesis, AI-slop audits, human-specificity
  revision, and reusable voice profiles. Do not use for detector evasion,
  fabricated personal stories, or specialized PR descriptions when ce-pr-description
  is a better fit.
user-invocable: true
tags: [writing, editing, voice, drafting, audit, humanize]
related: [research-gpt55, clarify, polish, ce-pr-description, ce-proof]
---

# writing

Create, revise, audit, and polish writing using human-specificity workflows: real substance before prose, genre-specific constraints, multi-candidate generation, best-parts synthesis, and span-level editing.

## Core principles

1. **Human substance before prose.** Human-like writing depends on real details, opinions, stakes, examples, and constraints.
2. **Genre beats tone.** Prefer specific context over vague adjectives like “casual” or “human.”
3. **Multiple candidates beat one-shot drafting.** For substantive work, explore variants before composing the final.
4. **Best-parts synthesis beats picking a winner.** Treat drafts as a parts bin unless the user asks for separate options.
5. **Span-level editing beats vague rewriting.** Identify weak spans, rewrite them, then integrate.
6. **Do not invent lived experience.** If human detail is missing, mark where the user should add it.
7. **Preserve useful roughness.** Human writing is not always perfectly symmetrical, polished, or complete.
8. **Optimize for reader trust, not detector scores.**

## Execution header

Before substantive work, set this state internally and show a one-sentence plan only when useful:

```text
MODE: blank_page | notes_to_draft | variants | revise | audit | humanize | voice_profile | finish
DEPTH: quick | standard | deep
INPUT_TYPE: none | notes | draft | samples | mixed
AUDIENCE: [inferred or stated]
VOICE_SOURCE: none | user_samples | requested_style | existing_draft
VARIANT_COUNT: 1 | 3 | 5-6
STOP_RULE: [what is enough for this request]
```

## Depth routing

- **quick**: one draft or edit + light audit. Use for low-stakes, urgent, or simple requests.
- **standard**: 3 variants + best-parts synthesis + final audit. Default for substantive writing.
- **deep**: 5–6 variants + scored tournament + composite + revision pass. Use when the user asks for best possible, many options, high-stakes communication, or “everything in between.”

## Mode routing

Infer the mode. Do not force the user to choose.

| Mode | Use when | Stop rule | Template/reference |
|---|---|---|---|
| `blank_page` | User gives topic/goal/format but little prose | final draft + missing-detail notes | `references/mode-routing.md` |
| `notes_to_draft` | User gives bullets, notes, transcript, rough ideas | organized draft preserving user substance | `references/mode-routing.md` |
| `variants` | User asks for options, quality matters, or deep exploration | composite stronger than any individual draft | `templates/draft-tournament.md` |
| `revise` | User provides draft and wants improvement | revised draft + brief change notes | `templates/revision-plan.md` |
| `audit` | User wants critique or diagnosis | verdict + span-specific fixes; rewrite only if requested/useful | `templates/audit-report.md` |
| `humanize` | User wants prose less AI-ish or more natural | revised text + missing-human-detail flags | `references/ai-slop-signals.md` |
| `voice_profile` | User provides samples or asks “write like this/me” | reusable voice profile | `templates/voice-profile.md` |
| `finish` | User asks for final polish/proofread | ready-to-send version | `templates/revision-plan.md` |

## Default workflow

For most substantive writing tasks:

1. Infer audience, purpose, format, stakes, and constraints.
2. Ask one focused clarification only if missing information would materially change the result. Otherwise proceed with stated assumptions.
3. Choose depth.
4. If standard/deep, run a draft tournament: generate distinct candidates, critique, harvest best parts, assemble composite.
5. Run AI-slop/human-specificity audit.
6. Provide final draft plus concise notes.

For quick tasks, produce the best single draft and a light note on assumptions.

## Humanization rules

Humanizing means making prose more specific, situated, natural, and trustworthy. It does **not** mean bypassing detectors.

Do:
- preserve meaning
- cut generic setup
- replace abstractions with concrete detail where the source supports it
- reduce over-polished transitions
- vary rhythm
- remove repeated AI-signature phrasing
- break overly symmetrical structure
- make endings quieter when appropriate
- keep useful roughness

Do not:
- add fake anecdotes, credentials, testimonials, citations, emotion, or personal experience
- add typos as a trick
- add slang without reason
- optimize for AI detector evasion

If the source lacks human detail, explicitly mark where the user should add it.

## Safety and integrity

Refuse or redirect requests to misrepresent authorship where disclosure is required, fabricate lived experience, forge credentials/testimonials, invent citations, or bypass AI detectors. Redirect toward reader-trust revision: clearer, more specific, better grounded, and more voice-consistent.

For external high-stakes communications, legal/medical/financial claims, or durable publication, recommend a human review pass and avoid unsupported factual claims.

## Adjacent-skill handoffs

- Use `research-gpt55` when factual research, citations, claim verification, or source-grounded synthesis is central.
- Use `ce-pr-description` for pull-request titles/bodies.
- Use `clarify` for narrow UX copy/microcopy improvements.
- Use `polish` for UI/interface polish where visual design is central.
- Use `ce-proof` when the user wants collaborative markdown review in Proof.

## Completion checklist

Before finalizing, check:

1. Does the writing fit audience and purpose?
2. Is there a clear point?
3. Does it preserve the user’s meaning?
4. Does it contain concrete human detail, or flag where detail is missing?
5. Are obvious AI-slop patterns reduced?
6. Is the rhythm varied enough for the genre?
7. Is the ending appropriate rather than over-neat?
8. Are assumptions and caveats visible when they matter?
