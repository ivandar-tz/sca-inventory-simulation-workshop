# Final Quiz Questions

This file stores the quiz questions that were approved during course-design discussions. The questions assess simulation reasoning rather than notebook syntax.

## Question 1: Dynamic state updates

**Topic:** Dynamic simulation, state updates, event sequence

**Material needed:** A small period-by-period inventory table showing inventory at start, arrivals, demand, satisfied demand, unmet demand, inventory at end, inventory position, and whether an order is placed.

**Question**

In this simulation, why is it important to update the inventory period by period instead of only comparing the total demand with the total supply?

A. Because the sequence of demand and replenishment determines whether inventory is available when demand occurs.

B. Because average inventory can only be calculated if inventory is updated every period.

C. Because comparing total demand with total supply ignores ordering cost and holding cost.

D. Because inventory position after ordering is always more important than inventory on hand.

**Correct answer:** A

**Explanation:**

Dynamic simulation matters because timing changes outcomes. Total supply over the full horizon may look sufficient, but stockouts can still occur if replenishment arrives after demand occurs.

**Distractor logic:**

- B is partly tempting because period-level inventory helps calculate average inventory, but it is not the main reason for dynamic simulation.
- C is plausible because costs matter, but the question is about timing and availability.
- D uses real terminology, but overstates inventory position. Inventory on hand is what satisfies demand.

**Simulation takeaway:**

Dynamic simulation is needed when the sequence of events affects system performance.

---

## Question 2: Input modelling and forecast quality

**Topic:** Input modelling, forecast bias, Relative MAE, Relative ME, trend

**Material needed:** A table comparing candidate demand models with Relative MAE, Relative ME, and whether a trend component is included.

**Important convention:**

Relative ME is calculated as:

`actual demand - forecast demand`

Therefore:

- positive Relative ME means underprediction;
- negative Relative ME means overprediction.

**Question**

Historical demand shows a visible upward trend. The selected model will be used as the demand input for an inventory simulation, where the stockout cost is high.

Which model is the most defensible starting point?

A. Model A, because it has the lowest Relative MAE, so its typical forecast error is smallest.

B. Model B, because it includes the trend component and has almost no systematic bias, even though its typical error is not the lowest.

C. Model C, because it includes the trend component and has a low Relative MAE and since the stockout costs are high, overpredicting is less important.

D. Model D, because it has low systematic bias and avoids adding a trend component.

**Correct answer:** B

**Explanation:**

The best input model for simulation is not automatically the one with the lowest MAE. The model should also avoid systematic bias and represent visible demand structure. Model B is defensible because it includes the trend and has almost no systematic bias.

**Distractor logic:**

- A is tempting because of low MAE, but it ignores bias and trend.
- C is tempting because it includes trend and may have a low MAE, but the interpretation depends on the ME sign. If C has positive ME, it is underpredicting, which is risky when stockout cost is high.
- D is tempting because of low bias, but avoiding a trend component is not a strength when the data visibly trend upward.

**Simulation takeaway:**

Input-model quality should be judged by the decision context. Bias and structural fit can matter as much as typical error.

---

## Question 3: Missing Monte Carlo evidence

**Topic:** Replications, stochastic outputs, output variability

**Material needed:** A consulting-report table comparing airport security staffing plans using average waiting time, share of passengers waiting below a threshold, staff cost, delay cost, and total cost.

**Question**

A consulting team evaluates three staffing plans for an airport security checkpoint. The simulation includes random passenger arrivals and random service times.

The report recommends Plan B because it has the lowest total cost and acceptable service.

What is the strongest simulation-related critique of this report?

A. The report discusses cost and service separately, but it does not define a service target or explain whether Plan C's additional service improvement is worth the extra cost compared with Plan B.

B. The report treats the simulation as a dynamic system, but average waiting time is not a state variable, so it should not be used as an output KPI.

C. The report states that arrivals and service times are random, but it does not show variability of the KPI results across simulation runs.

D. The report should first report MAE and ME for the passenger-arrival model, because without forecast accuracy metrics the staffing recommendation cannot be evaluated.

**Correct answer:** C

**Explanation:**

If the simulation has random arrivals and random service times, its KPI outputs are random. A table of point estimates is not enough. The report should show variability across runs, such as confidence intervals, ranges, percentiles, or distributions.

**Distractor logic:**

- A is a valid management critique, but the strongest simulation-method issue is missing output variability.
- B confuses state variables with output KPIs. Average waiting time is a valid KPI.
- D is plausible because input modelling matters, but the visible weakness is missing stochastic output variability.

**Simulation takeaway:**

Stochastic simulation results should be reported with uncertainty, not only as point estimates.

---

## Question 4: Experiment-grid design

**Topic:** Experiment grid, confidence intervals, boundary solution

**Material needed:** A plot showing mean waiting time and mean total cost by staffing level, with confidence intervals. The tested staffing levels end at 10, and 10 is the best tested point.

**Question**

A consulting team uses a stochastic simulation to test staffing levels at a service facility. The figure shows the mean waiting time and mean total cost for each tested staffing level, with confidence intervals.

Based on the figure, what is the most appropriate conclusion?

A. Choose 10 staff, because it has the lowest mean waiting time and the lowest mean total cost among the tested alternatives.

B. Run more replications before comparing alternatives, because the confidence intervals make the ranking of all staffing levels too uncertain.

C. Expand the staffing grid beyond 10 staff, because the best tested option is at the boundary of the experiment and lower costs may exist outside the tested range.

D. Choose 9 staff, because it already provides acceptable waiting time with fewer staff.

**Correct answer:** C

**Explanation:**

The figure may show that 10 staff is best among the tested alternatives, but it is also the largest tested value. If the best result is at the boundary, the experiment has not shown whether better values exist outside the tested grid.

**Distractor logic:**

- A is tempting because it reads the tested results correctly, but it overclaims optimality.
- B is plausible because uncertainty matters, but the main issue here is the experiment range.
- D is tempting as a service-cost argument, but it assumes a service target that has not been defined.

**Simulation takeaway:**

A simulation experiment only compares the alternatives that were tested. Edge-of-grid results require further testing.

---

## Question 5: Final decision under risk

**Topic:** Decision profile, service risk, expected cost, downside risk

**Material needed:** A policy table showing mean total cost, 95th percentile total cost, mean service level, and probability that service falls below 95%.

**Question**

A retailer is choosing an inventory policy for a high-priority product family. The simulation results are shown in a table.

Management says:

> Service level is crucial: we do not want a policy that frequently falls below 95% service. At the same time, we cannot simply choose the most expensive high-service option. We want a policy with acceptable expected cost and limited downside risk.

Which recommendation best matches this decision profile?

A. Policy A

B. Policy B

C. Policy C

D. Policy D

**Correct answer:** B

**Explanation:**

Policy B best matches the stated profile if it offers acceptable expected cost, satisfies service expectations, and limits the probability of falling below the service threshold. It avoids the high downside risk of a cheaper policy and avoids the excessive cost of the safest policy.

**Distractor logic:**

- Policy A is tempting if focusing on expected cost, but it has too much downside service risk.
- Policy C is tempting if focusing on service only, but management does not want the most expensive high-service option.
- Policy D is tempting if focusing on lowest cost, but it violates the service priority.

**Simulation takeaway:**

Simulation does not choose the policy automatically. The recommendation depends on the decision-maker's risk profile and business priorities.

---

## Notes

These approved questions are strong because they require students to apply simulation concepts to evidence. They should be used as anchors for future question generation.

Future question development should add one more hard question on confidence intervals and comparison strength, preferably using a table or plot with overlapping intervals where the correct conclusion is not simply “choose the lower mean”.
