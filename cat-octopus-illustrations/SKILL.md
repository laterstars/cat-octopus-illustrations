---
name: cat-octopus-illustrations
description: Turn a short prompt into one clean, hand-drawn concept illustration starring a calm Cat-Octopus. Use when the user gives an idea, judgment, process, feeling, or metaphor as a short prompt and wants a single Cat-Octopus illustration, concept sketch, explainer image, article figure, or visual for it. The default style is a black cat–octopus hybrid with a pale face, pointed ears, whiskers, a curled tail, and several short working tentacles; black hand-drawn line art on white; one warm-orange accent; lots of whitespace; one idea per image; then generated.
---

# Cat-Octopus Illustrations

## Core idea

Turn a short prompt into one 16:9 hand-drawn concept illustration. The goal is not commercial art, a PPT infographic, or a cute cartoon—it is to take a single idea (a judgment, process, contrast, state, or metaphor) and draw it as a clean, calm, slightly absurd sketch that reads in about one second.

The recurring character is **the Cat-Octopus**: a black cat–octopus hybrid with a large rounded cat head, pointed ears, whiskers, a pale oval face, large vertical eyes, a curled tail, and an octopus-like lower body with several short tentacles. Its expression is calm, friendly, and quietly confident while it gravely performs a mildly ridiculous job. The Cat-Octopus must perform the core action of the image, not stand beside it as decoration. Its tentacles should be functional whenever the action calls for handling, sorting, connecting, carrying, repairing, or coordinating.

Input is a **short prompt**, not an article. The user already knows the idea; this skill's job is to invent a fitting visual metaphor, put the Cat-Octopus to work inside it, and draw it well.

## The contract: compose first, then draw

For each prompt, **think briefly out loud, then generate one image**. Before calling the image model, state:

- **Metaphor** — the fresh low-tech metaphor you invented for this prompt.
- **Cat-Octopus's action** — what the Cat-Octopus is physically doing to drive the idea.
- **Labels** — the short English handwritten labels that will appear (a few; at most 5–8).
- **Composition** — where the Cat-Octopus sits, the main object, and how the eye moves.

Then generate **one** image. One prompt → one composed image. Do not fan out into variations unless the user asks. If the user gives several prompts, make one image for each.

## Read these references as needed

Pull in only what the task needs; do not load everything at once:

- `references/style-dna.md` — the visual DNA: line, color (single warm-orange accent), whitespace, and hard nos.
- `references/cat-octopus-character.md` — the Cat-Octopus's form, personality, action vocabulary, and don'ts.
- `references/composition-patterns.md` — structure types and how to invent a fresh metaphor every time.
- `references/prompt-template.md` — the fill-in-the-blanks single-image generation prompt.
- `references/qa-checklist.md` — post-generation checks and iteration moves.

## Workflow

### 1. Read the prompt

Take the user's short prompt and decide what *kind* of idea it is: a judgment, an input→output process, a before/after contrast, a character/user state, or a concept metaphor. That choice determines the structure type. Do not over-interpret a one-liner into a whole article—illustrate the single idea in front of you.

### 2. Compose (think briefly)

State the metaphor, the Cat-Octopus's action, the labels, and the composition (see "The contract" above). Keep it to a few lines—enough for the user to catch a wrong take in one second, not an essay.

### 3. Generate one image

If the user clearly asks to generate, do not stop for confirmation—use the built-in image tool and produce one image with the prompt template. Each prompt must include:

- 16:9 horizontal concept illustration
- pure black background
- white hand-drawn line art
- exactly one warm-orange accent color (no other colors)
- lots of blackspace
- the Cat-Octopus as the subject performing the core action
- a few short handwritten English labels
- a quiet lower-right margin for the watermark
- no PPT look, no commercial illustration, no childish cuteness, no complex architecture diagram, and no top-left type-title

Invent a fresh metaphor for every prompt. Do not reuse a metaphor from a previous image unless the user explicitly asks to reuse or remix one.

### 4. Check and iterate

Run `references/qa-checklist.md`. Regenerate or make a local edit if:

- the Cat-Octopus is only decorative
- its tentacles do not contribute to the action when they reasonably could
- the canvas is too full
- it looks like a flowchart or slide
- there is too much text or garbled text
- a type-title appears in the top-left corner
- the style drifts toward cute, childish, overly polished, or stiff
- a second accent color crept in, or the background is not clean white

### 5. Save and report

If working inside a workspace, copy the final image to:

```text
assets/<prompt-slug>-illustrations/
```

Name images in order:

```text
01-topic-name.png
02-topic-name.png
```

Keep the original generated file and the unwatermarked generated source. Do not overwrite existing assets unless the user asks to replace them.

## Output register

Keep the pre-generation "compose" note short and concrete. After generating, report:

- how many images were made
- what each one depicts
- the save path

Let the image do the talking; do not lecture about style theory.
