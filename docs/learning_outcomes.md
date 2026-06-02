# Learning Outcomes

This workshop teaches simulation reasoning through an inventory-management application. Students should understand not only how to run a notebook, but how to interpret simulation evidence and use it to support operational decisions.

## Core learning outcomes

By the end of the workshop and assignment, students should be able to:

1. Explain why dynamic simulation updates a system state period by period.
2. Distinguish deterministic simulation from stochastic simulation.
3. Identify the role of random variables and random number generation in representing uncertain inputs.
4. Analyse historical demand data and select a defensible demand/input model.
5. Interpret forecast metrics such as Relative MAE and Relative ME when evaluating simulation inputs.
6. Design a simulation experiment comparing inventory policies.
7. Run and interpret Monte Carlo replications.
8. Compare policies using service, cost, stockout, inventory, and robustness metrics.
9. Interpret confidence intervals and variability across replications.
10. Make an evidence-based recommendation under service, cost, and risk constraints.

## Assignment evaluation outcomes

The group assignment is evaluated using four main criteria.

### 1. Input analysis and demand model choice

Students should analyse the sales data, identify relevant demand patterns, and justify the selected expected-demand model or uncertainty assumption using diagnostics and forecast metrics.

Relevant evidence may include demand level, variability, trend, calendar structure, Relative MAE, and Relative ME.

### 2. Experiment design, RNG, and simulation setup

Students should build a coherent stochastic simulation setup. This includes the demand RNG, policy grid, time horizon, number of replications, lead time, and cost parameters.

The tested values of `r` and `Q` should be scaled to the demand level of the product family.

### 3. Trade-off and robustness interpretation

Students should interpret service-cost trade-offs and robustness under uncertainty. They should not simply select the policy with the lowest mean cost.

Relevant evidence may include confidence intervals, variability across replications, probability of poor service, high-cost outcomes, and sensitivity to cost assumptions.

### 4. Final recommendation quality

Students should make a clear recommendation for each product family. The recommendation should include the selected `(r, Q)` policy, expected service level, expected cost, main trade-off, limitations, and what should be tested next.

## Main teaching progression

The learning sequence is:

1. deterministic state updates and inventory KPIs;
2. stochastic demand and random input generation;
3. repeated runs and Monte Carlo logic;
4. policy experiments and comparison of alternatives;
5. real-data demand modelling and management recommendation.
