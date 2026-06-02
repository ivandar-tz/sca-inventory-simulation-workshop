# Question Design Rules

This document defines the rules for creating quiz questions for the inventory simulation workshop.

The quiz should assess simulation reasoning. It should not primarily assess coding memory, syntax, or whether students remember exact notebook variable names.

## What makes a good question

A good question asks students to interpret evidence and make a defensible judgement. The best questions use a realistic scenario, table, plot, or short report.

Good question stems include:

- What is the strongest simulation-related critique?
- What is the most defensible conclusion?
- What should the analyst do next?
- Which recommendation best matches the decision profile?
- Which model is the most defensible simulation input?

## What “hard” means

Hard does not mean confusing. A hard question should require students to apply workshop concepts carefully.

Hard questions should:

- combine more than one idea when appropriate;
- require interpretation rather than recall;
- use plausible distractors;
- reward students who attended class and understood the workshop;
- avoid giving away the answer through wording.

## Multiple-choice rules

Multiple-choice questions are acceptable, but the options must be balanced.

Rules:

1. Use four answer options.
2. Avoid obviously silly wrong answers.
3. Avoid making the correct answer much longer or more carefully worded than the others.
4. Distractors should reflect common analytical mistakes.
5. Avoid options that are technically true but irrelevant unless the task asks for the strongest critique.
6. Avoid absolute wording such as “always”, “never”, or “cannot” unless it is intentionally part of the distractor.
7. Do not make the correct answer obvious from the phrasing.

## Useful distractor types

Good distractors include:

- choosing the lowest expected cost while ignoring service risk;
- choosing the highest service level while ignoring cost;
- confusing state variables with output KPIs;
- confusing input-model quality with output uncertainty;
- thinking that testing many alternatives once is the same as running replications;
- recommending the best tested edge-of-grid solution as final optimum;
- asking for more replications when the real issue is a narrow experiment grid;
- ignoring confidence intervals;
- treating simulation output as exact truth;
- treating a low MAE as sufficient even when the model is biased;
- assuming a service-cost trade-off is resolved without a service target.

## Preferred evidence types

Use these evidence formats when possible:

1. A small state-update table.
2. A forecast-model comparison table.
3. A consulting report output table.
4. A plot of simulation results with confidence intervals.
5. A policy-risk table showing mean cost, service, downside risk, and tail outcomes.

## Answer explanation format

Each question should include:

- correct answer;
- why the answer is correct;
- why the distractors are tempting but insufficient;
- the simulation takeaway.

## Concepts to emphasise

The quiz should cover the following simulation concepts:

1. Dynamic state updates: timing and sequence matter.
2. Input modelling: simulation results depend on the demand/input model.
3. Monte Carlo replications: one run is one possible future.
4. Output uncertainty: means should be interpreted with variability or confidence intervals.
5. Experiment design: the simulation only compares tested alternatives.
6. Robustness: expected performance is not enough when downside risk matters.
7. Decision alignment: the best policy depends on cost, service, risk, and business priorities.
