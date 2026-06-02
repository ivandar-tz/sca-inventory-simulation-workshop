# Quiz Blueprint

This document defines the target structure for hard quiz questions in the inventory simulation workshop.

The quiz should test simulation reasoning rather than notebook syntax. Inventory is the main application context, but questions may also use warehouses, airports, call centres, service systems, or transport operations.

## Core quiz sequence

A strong six-question quiz should move from model mechanics to decision judgement.

### 1. Dynamic state and event sequence

Tests whether students understand why simulation updates a system state period by period.

Typical evidence:

- state-update table;
- inventory path;
- queue evolution;
- daily demand and replenishment sequence.

Core idea:

> Totals are not enough because timing and sequence can create stockouts, waiting, queues, or unmet demand.

### 2. Input modelling and forecast quality

Tests whether students can judge which input model is defensible for simulation.

Typical evidence:

- table with Relative MAE, Relative ME, and trend component;
- demand plot with trend or structure;
- model comparison summary.

Core idea:

> The best simulation input is not automatically the model with the lowest MAE. Bias, trend, and structural fit matter because they affect simulated outcomes.

### 3. Replications and stochastic output

Tests whether students understand why stochastic simulations require repeated runs and variability reporting.

Typical evidence:

- consulting report with point estimates only;
- repeated runs of the same policy;
- output table missing variability.

Core idea:

> One run is one possible future. Monte Carlo replications are needed to estimate the distribution of outcomes.

### 4. Confidence intervals and comparison strength

Tests whether students can compare uncertain simulation outputs without overclaiming.

Typical evidence:

- mean KPI table with confidence intervals;
- service-cost plot with uncertainty bands;
- overlapping intervals across alternatives.

Core idea:

> A lower mean is not always enough to claim one policy is better if differences are small relative to uncertainty.

### 5. Experiment-grid design

Tests whether students understand that simulation only compares the alternatives that were tested.

Typical evidence:

- plot where the best tested alternative is at the boundary;
- policy grid where all improvements point in one direction;
- experiment range that is too narrow.

Core idea:

> If the best solution is at the edge of the grid, the next step is to expand or refine the experiment rather than claiming a final optimum.

### 6. Final decision under risk

Tests whether students can align simulation evidence with a decision-maker's priorities.

Typical evidence:

- policy table with mean cost, tail cost, mean service, and probability of service failure;
- management profile describing service, cost, and risk preferences.

Core idea:

> Simulation does not choose automatically. The recommendation depends on expected performance, service requirements, downside risk, and business priorities.

## Integrated question combinations

Harder questions may combine more than one topic.

Useful two-topic combinations:

1. Dynamic state updates + input modelling
2. Input modelling + decision risk
3. Replications + output variability
4. Confidence intervals + decision under risk
5. Experiment grid + confidence intervals
6. Experiment grid + decision under risk

Useful three-topic combinations:

1. Input modelling + replications + decision under risk
2. Confidence intervals + experiment grid + decision under risk

Useful four-topic combination:

1. Input modelling + replications + confidence intervals + decision under risk

## Recommended final six-question quiz

A strong final quiz can use the following order:

1. Dynamic state + input modelling
2. Input modelling + decision risk
3. Replications + output variability
4. Experiment grid + confidence intervals
5. Confidence intervals + decision under risk
6. Input modelling + replications + decision under risk

This progression tests:

1. whether students can read a dynamic system;
2. whether they can choose credible stochastic inputs;
3. whether they can detect weak Monte Carlo evidence;
4. whether they can critique experiment design;
5. whether they can interpret uncertainty in decisions;
6. whether they can make an integrated simulation-based judgement.

## Difficulty standard

Questions should be hard because they require simulation reasoning, not because they are confusing.

A hard question should require students to:

- apply concepts from class and workshop;
- interpret evidence;
- choose among plausible alternatives;
- distinguish between different types of methodological weakness;
- make a defensible judgement under uncertainty.
