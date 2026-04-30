# Pressure Test: Voice Profile

## User request

Here are three samples of my writing. Create a style guide I can reuse.

## Expected behavior

- Infer `voice_profile`.
- Use `templates/voice-profile.md`.
- Label confidence based on sample count/diversity.
- Extract concrete habits, not vague adjectives.
- Include reusable prompt block.
- Do not save profile unless explicitly asked.

## Failure mode

- “Your style is clear, engaging, and thoughtful” without operational details.
- Overfitting one unusual phrase.
- Applying the voice immediately when the user only asked for a guide.
