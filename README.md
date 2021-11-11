# AL-in-CreditScoring
Active Learning in Credit Scoring – project for my Master's Thesis

A benchmarking experiment using multiple Active Learning (AL) algorithms on several credit scoring datasets.
This experiment evaluates if credit scorecards improve their predictive power when being assisted by Active Learning methodology. 
The experiment is motivated by the fact that all credit scoring data is biased, because the data only contains samples who received a loan in the past: 
Since loan-granting decisions are often aided by predictive models or heuristics trying to only predict good debtors, the population of loan receivers is (increasingly) different from the population of loan applicants. Over time, this can have negative long term effects on predictive power.

The main hypotheses is that AL could help the scorecard's predictive power (generalizability) by selecting certain samples from the applicant population that the current scorecard would otherwise reject. In a round-based experiment, with loan applications being selected by both their score (based on current scorecard model) plus AL methodology, the experiment analyzes if scorecard performance improves compared to a standard model where samples are only selected by their score.

It further examines whether any improvement in predictive power is worth the risk (and thus cost) of having AL select instances the scorecard deemed bad debtors. After all, any false negative (a BAD case predicted GOOD) is very costly. Implementing AL would only then make sense in a real-world application when the gain in predictive power on future applicants offsets the increased cost of accepting potentially bad loans in the current period.
