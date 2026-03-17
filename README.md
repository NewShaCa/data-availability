# processed_data.csv – Trust Game Behavioral Dataset

## Overview

This file contains the processed behavioral dataset from a repeated trust game experiment.  
The data are organized at the **trial level**, meaning that each row represents a single trial completed by a participant.
Participants repeatedly decided how much money to invest with a trustee across multiple trials. In each trial, the trustee returned a certain amount of money, and participants evaluated the trustee's behavior.
This dataset contains decision variables, reaction times, feedback variables, and experimental condition indicators used in the statistical analyses reported in the manuscript.
## Data structure

- **Unit of observation:** trial
- **Rows:** individual trials for each participant
- **Participants:** each participant appears across multiple rows
- **Groups:** participants belong to either a clinical group (`case`) or a healthy control group (`control`)

## Variables
### Participant information
- **Participant_ID**  
  Numeric identifier assigned to each participant.


- **Male_1**  
  Binary gender variable  
  - 1 = male  
  - 0 = female

- **group**  
  Participant group classification  
  - `case` = clinical group  
  - `control` = healthy control group

---

### Trial information

- **Trial_Number**  
  Sequential trial number within the experiment.

- **Order_Shuffle**  
  Index indicating the randomized order of trials presented to the participant.

- **Payback_Shuffle**  
  Index indicating the randomized schedule of trustee returns.

---

### Decision variables

- **Money_Transfered**  
  Amount of money invested by the participant in the trustee during the trial.

- **RT_Investment**  
  Reaction time (in seconds) for the participant's investment decision.

---

### Trustee feedback

- **Amount_Returned**  
  Amount of money returned by the trustee to the participant during the feedback stage.

- **RT_Feedback**  
  Reaction time recorded during the feedback stage.

---

### Experimental conditions

- **Fair**  
  Indicator of fairness condition of the trustee's behavior.

- **Happy**  
  Indicator of the trustee's facial expression condition.

These variables represent experimental manipulations used to examine how fairness and emotional cues influence trust decisions.

---

### Evaluation measures

- **Eval**  
  Participant's evaluation of the trustee's fairness on that trial.

- **RT_Evaluation**  
  Reaction time for the evaluation response.

---

### Block-level evaluations

Participants may also provide evaluations after a block of trials.

- **Eval_self**  
  Participant’s evaluation of their own behavior.

- **RT_eval_self**  
  Reaction time for self-evaluation.

- **Eval_other**  
  Participant’s evaluation of the trustee.

- **RT_eval_other**  
  Reaction time for evaluation of the trustee.

---

### Payoff variables

- **Final_money_subj**  
  Accumulated payoff for the participant.

- **Final_money_trustee**  
  Accumulated payoff for the trustee.

These variables track cumulative earnings during the experiment.

---

## Notes

- The dataset is already **processed and organized for statistical modeling**.
- Observations are **not independent**, since multiple trials belong to the same participant.
