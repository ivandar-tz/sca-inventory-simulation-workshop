# Codex Instructions

This repository supports the SCA inventory simulation workshop. Codex should help maintain teaching material, notebooks, scripts, data-generation utilities, quiz assets, and assessment documents.

## Core principle

Do not change pedagogy or modelling logic unless explicitly requested. Codex should mainly help with implementation, cleanup, consistency, and repeatability.

## Course context

The workshop teaches undergraduate Industrial Engineering students how to use simulation for inventory and operations decisions. Inventory is the application context, but the central learning goal is simulation reasoning:

- dynamic state updates
- stochastic demand and random number generation
- Monte Carlo replications
- confidence intervals and output uncertainty
- experiment design
- service-cost trade-offs
- robustness and decision-making under risk

## Notebook rules

When editing notebooks:

1. Preserve the teaching sequence.
2. Keep markdown explanations clear and concise.
3. Clearly mark cells where students must input values.
4. Do not remove explanatory text unless requested.
5. Do not silently change model logic.
6. Keep teaching, student, and solution versions aligned.
7. Avoid hidden dependencies between distant cells when possible.
8. Prefer self-contained cells for important visualisations and checkpoints.
9. Do not write CSVs, figures, or other output files unless explicitly requested by the task.
10. If output files are needed, write them to `outputs/` or another explicitly requested folder.

## Student-version rules

When creating or editing student notebooks:

1. Replace only explicitly prompted student inputs with placeholders such as `xxxx`.
2. Do not remove structural code needed for the notebook to run.
3. Replace answer text with prompts such as `Type here your answer`.
4. Keep enough guidance so students know what they are expected to change.
5. Do not expose solution logic in markdown.

## Solution-version rules

When creating or editing solution notebooks:

1. Provide working parameter values.
2. Include answer keywords rather than overly long model answers when the purpose is grading.
3. Keep explanations aligned with the teaching version.

## Script rules

When writing scripts:

1. Keep functions reusable and documented.
2. Avoid hard-coded absolute paths.
3. Use relative paths from the repository root.
4. Do not overwrite existing files without explicit instruction.
5. Print or preview results before writing files when the task involves data creation.
6. Keep generated data separate from raw data.

## Data rules

1. Do not commit large raw datasets unless explicitly approved.
2. Keep raw data in `data/raw/` and generated data in `data/generated/`.
3. Keep small curated teaching datasets in `data/processed/` only if they are needed for students.
4. Document how generated or calibrated datasets were created.

## Quiz and assessment rules

When generating quiz questions:

1. Follow `quizzes/briefs/question_design_rules.md` if present.
2. Questions should test simulation reasoning, not notebook memory.
3. Prefer realistic scenarios, tables, or plots.
4. Multiple-choice distractors must be plausible.
5. Avoid silly wrong answers.
6. Avoid trick wording.
7. Include the correct answer and a short explanation.
8. Include why the distractors are tempting but insufficient.
9. Hard questions should require applying concepts, not decoding confusing language.

## Slides and figures

When editing slides or generating figures:

1. Keep the visual style clean and suitable for undergraduate teaching.
2. Avoid cluttered plots.
3. Label uncertainty clearly when shown.
4. Do not include code on slides unless the slide is explicitly about code.
5. Preserve editable source files when possible.

## Git workflow

1. Make small, coherent commits.
2. Use clear commit messages.
3. Do not mix unrelated changes in one commit.
4. When unsure, propose a plan before editing files.
