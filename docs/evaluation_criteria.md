# Evaluation Criteria

This document defines the main criteria for evaluating the group dashboard assignment and related simulation assessment tasks.

## Criterion 1: Input analysis and demand model choice

Evaluate whether students analyse the input data before running the simulation.

Strong work should:

- describe the demand level and variability of each product family;
- identify relevant demand patterns such as trend, calendar structure, volatility, or intermittency;
- compare candidate demand models using appropriate diagnostics;
- interpret Relative MAE as typical forecast error;
- interpret Relative ME as systematic underprediction or overprediction;
- justify the selected input model in relation to the simulation decision.

Weak work usually:

- selects the model with the lowest MAE without discussing bias;
- ignores visible demand patterns;
- treats the demand input as a neutral technical detail;
- fails to explain how input assumptions affect simulated inventory outcomes.

## Criterion 2: Experiment design, RNG, and simulation setup

Evaluate whether students design a coherent simulation experiment.

Strong work should:

- define sensible `r` and `Q` ranges for each product family;
- scale the policy grid to the demand level;
- choose a reasonable simulation horizon;
- use enough replications to assess stochastic performance;
- report lead-time and cost parameters;
- explain the role of the demand RNG;
- recognise when a tested grid is too narrow or when the best policy is at the boundary.

Weak work usually:

- uses arbitrary policy values;
- applies the same grid to very different product families without justification;
- reports only one simulation run;
- ignores the role of random demand;
- treats the best tested option as globally optimal without checking the experiment range.

## Criterion 3: Trade-off and robustness interpretation

Evaluate whether students interpret the simulation output critically.

Strong work should:

- compare policies using service level, total cost, inventory, unmet demand, and cost components;
- discuss the service-cost trade-off;
- use confidence intervals or variability across replications;
- identify robust and risky policies;
- consider the probability of poor service or high-cost outcomes;
- recognise when policies are not meaningfully different.

Weak work usually:

- selects the lowest mean cost without checking service;
- selects the highest service without checking cost;
- ignores confidence intervals;
- treats simulation estimates as exact values;
- reports plots or tables without interpretation.

## Criterion 4: Final recommendation quality

Evaluate whether students turn simulation evidence into a management-facing recommendation.

Strong work should:

- recommend one policy per product family;
- report expected service level and expected cost;
- explain the main trade-off behind the recommendation;
- discuss downside risk and remaining uncertainty;
- compare how the recommendation differs across product families;
- state what should be tested next before implementation.

Weak work usually:

- gives a vague recommendation;
- does not connect the recommendation to the evidence;
- ignores business priorities;
- overclaims precision;
- fails to mention limitations or next steps.

## Overall judgement

A strong submission should show the complete analytical chain:

`data input -> demand model -> stochastic simulation -> experiment design -> output uncertainty -> policy recommendation`

The best submissions are not those that simply find the cheapest policy. They are those that make a defensible recommendation while explaining why the result is credible, uncertain, and conditional on assumptions.
