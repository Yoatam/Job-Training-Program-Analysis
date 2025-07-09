# Job-Training-Program-Analysis
This project explores a fundamental question in public policy:

> **Did a job training program actually help disadvantaged workers earn more?**

Using data from a real-world study in the 1980s, I applied modern **causal inference** techniques to estimate the true effect of the program—accounting for background differences between those who enrolled and those who didn’t.

---

## 📌 Project Overview

This analysis revisits the **National Supported Work Demonstration**, a program aimed at helping high-risk individuals — such as ex-offenders, high school dropouts, and the long-term unemployed — transition into the workforce.

Using the **Lalonde dataset**, I evaluate whether participating in this job training program *causally* improved future earnings.

---

## ❓ Key Questions

- Did the job training program actually cause an increase in earnings?
- Were there differences in background characteristics between those who enrolled and those who didn’t?
- After balancing for these differences, does the treatment still show a positive effect?

---

## 📂 Dataset

**Lalonde Dataset (1986)**  
Contains 11 variables for 445 individuals:

- **Demographics:** `age`, `educ`, `black`, `hisp`, `married`, `nodegr`
- **Historical earnings:** `re74`, `re75` (pre-treatment)
- **Outcome:** `re78` (post-treatment earnings)
- **Treatment indicator:** `treat`

---

## ⚙️ Methods

To estimate the **Average Treatment Effect (ATE)**, I applied both statistical and machine learning methods.

### Propensity Score Estimation using:
- Logistic Regression
- Decision Trees
- Random Forests

### Matching Techniques:
- Nearest-neighbor matching based on estimated propensity scores

### Covariate Balance Assessment:
- Standardized differences before and after matching
- Visual comparisons of matched vs. unmatched distributions

---

## 🔍 Key Findings

- Without adjusting for covariates, treated individuals appeared to earn more — but this was misleading due to background differences.
- After matching using propensity scores (especially from **Random Forests**), the estimated treatment effect was **smaller but still positive**.
- Covariate balance improved significantly after matching, increasing confidence in the causal interpretation.

---

## ⚠️ Limitations

- Assumes **no hidden confounders** — unmeasured variables may still bias results.
- Matching quality depends on **accuracy of propensity score models**.
- **Limited external validity** — findings apply to populations similar to the study sample.

---

## ▶️ How to Run

1. **Clone this repository:**
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
2. **Install required Python packages:**
   ```bash
   pip install -r requirements.txt


  📁 Note: The dataset lalonde.csv is included for full reproducibility.
