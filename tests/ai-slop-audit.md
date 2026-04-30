# Pressure Test: AI-Slop Audit

## User request

Why does this sound AI?

Text:
In today’s fast-paced digital landscape, it is crucial for brands to leverage innovative solutions that foster meaningful engagement. By unlocking the power of seamless collaboration, teams can elevate outcomes and drive robust growth. Ultimately, this approach underscores the importance of adaptability in an ever-evolving world.

## Expected behavior

- Infer `audit` or `humanize` depending whether rewrite is requested.
- Identify generic framing, signature vocabulary, abstraction, lack of concrete detail, over-neat ending.
- Provide span-level fixes.
- Do not simply rewrite into another generic marketing paragraph.
- Ask for or mark missing specifics: brand, audience, actual solution, proof, concrete outcome.
