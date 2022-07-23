# AL-in-CreditScoring
Active Learning in Credit Scoring – Masters Thesis Project

A benchmarking experiment using multiple Active Learning (AL) algorithms on several credit scoring datasets.
This experiment evaluates if credit scorecards improve their predictive power when being assisted by Active Learning methodology. 
The experiment is motivated by the fact that all credit scoring data is biased, because the data only contains samples who received a loan in the past: 
Since loan-granting decisions are often aided by predictive models or heuristics trying to only predict good debtors, the population of loan receivers is (increasingly) different from the population of loan applicants. Over time, this can have negative long term effects on predictive power.

The main hypotheses is that AL could help the scorecard's predictive power (generalizability) by selecting certain samples from the applicant population that the current scorecard would otherwise reject. In a round-based experiment, with loan applications being selected by both their score (based on current scorecard model) plus AL methodology, the experiment analyzes if scorecard performance improves compared to a standard model where samples are only selected by their score.

It further examines whether any improvement in predictive power is worth the risk (and thus cost) of having AL select instances the scorecard deemed bad debtors. After all, any false negative (a BAD case predicted GOOD) is very costly. Implementing AL would only then make sense in a real-world application when the gain in predictive power on future applicants offsets the increased cost of accepting potentially bad loans in the current period.


## HOW TO USE THE CODE
All files required are part of the repo, except the datasets, which can be found here:
https://bit.ly/3cv08Xb (Google Drive Folder)

The full code of the experiment comprises 4 code files:
- main file: AL_CreditScoring.ipynb
- parameter tuning: AL_CV.ipynb
- threshold tuning: threshold_tuner.ipynb
- result processing, plotting: result_processor.ipynb

The main file can be run without running the tuning first. For this to work, there are several secondary files required, which all also part of the repo. Namely, the tuned parameters for each model, as received from the parameter tuning file. These are stored on the folder 'metaparameters'.
Also, the file containing the tuned thresholds for each dataset is needed ('NEW_tuned_thresholds').

**It is recommended to copy all files from the repo, plus the datasets needed, into a Google Drive folder from which the code can be run via Colab. Running locally is of course possible, but will require more adjustments to file paths etc., as well slight changes to the install routine of the libraries required.**

