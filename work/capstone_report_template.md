# Capstone Report — <your lane>

- **Author:** Tayyaba Noor
- **Lane:**   ML
- **Repo:**  https://github.com/Tayyaba1206/FlyRank-Internship
- **Date:**  30/072026

> Copy this file to `work/capstone_report.md` and fill it in as you build. Sections 1–8
> mirror the Pass / Needs-Work rubric axes, so nothing here is optional. Sections 0 and 9
> are **paper sections**: your deployed research paper must carry both, and they're here so
> you never rebuild them from memory at ship time.

## 0. Abstract

This project investigates whether machine learning can improve the ranking of pages for content refresh opportunities. An anonymized FlyRank internship dataset was used to build and evaluate several predictive models. The models were compared against a simple rule-based baseline using the same validation strategy. Random Forest produced the strongest overall ranking performance. The resulting ranked action queue is intended to support human decision-making rather than replace it.

## 1. Problem framing

The project supports content review decisions by ranking pages according to their refresh priority. Each row represents a content page. The output is a ranked review queue with reason codes. Human reviewers use these recommendations to prioritize their work. Incorrect recommendations may lead to unnecessary reviews or missed improvement opportunities. Machine learning helps identify useful patterns from historical search and engagement signals.

## 2. Data safety

Only anonymized and public-safe features were used. Client names, URLs, private queries, and sensitive identifiers were excluded. Leakage risks were reviewed by ensuring that no future or target-derived information was included in the training features.

## 3. Baseline

A transparent rule-based scoring method was implemented as the baseline. The same evaluation strategy was used for both the baseline and machine learning models to ensure a fair comparison.

## 4. Model / analysis

Random Forest was selected as the final model after comparing Logistic Regression and Decision Tree. The model used observable search, engagement, and content metrics while excluding leakage-prone features.

## 5. Evaluation

All models were evaluated using the same train-test split. Random Forest achieved the strongest overall ranking performance compared with the baseline. Results are presented using decision-support language without causal claims.

## 6. Interpretation

The model identified combinations of visibility, engagement, and content quality signals that were associated with higher refresh priority. Feature importance analysis improved the interpretability of the recommendations.

## 7. Recommendation

The ranked review queue should be used to prioritize manual content reviews. Recommendations are accompanied by reason codes and confidence levels. Human review remains essential before any action is taken.

## 8. Reproducibility

The project can be reproduced by cloning the repository, installing the requirements, and executing all notebooks from top to bottom. Random seeds were fixed to improve reproducibility.

## 9. Acknowledgments & data credit

Built on the FlyRank ML Internship dataset.

https://flyrank.ai

---

> **Claims checklist before submitting:** observed / measured / directional / decision-support
> **Metrics vs. base rate:** report your task's base rate (majority-class %) next to any
> precision@K or accuracy — a high score can just be a high base rate. AUC / lift over
> baseline are the honest discrimination numbers.
> language everywhere · no causal claims without an experiment or causal design · no
> "predicted Google's algorithm" · no client-identifying details · numbers in this report
> match a fresh re-run.
