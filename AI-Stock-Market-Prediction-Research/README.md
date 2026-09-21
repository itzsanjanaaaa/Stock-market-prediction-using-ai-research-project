# AI in Finance: Stock Market Prediction Using AI and ML — A Systematic Literature Review

[![Type](https://img.shields.io/badge/Project%20Type-Literature%20Review-blue)]()
[![Status](https://img.shields.io/badge/Status-Completed-brightgreen)]()
[![Field](https://img.shields.io/badge/Field-AI%20%2F%20FinTech-orange)]()
[![License](https://img.shields.io/badge/License-Academic%20Use-lightgrey)]()

> A systematic literature review examining how Artificial Intelligence and Machine
> Learning techniques have been applied to stock market prediction, synthesized
> from 19 peer-reviewed studies and covering classical ML, deep learning, ensemble/hybrid
> methods, and sentiment-driven approaches.

---

## Academic Context

This repository presents a **Research Methodology project** completed as part of the
6th-semester curriculum of the **B.Sc. (Hons.) Computer Science** program.

| | |
|---|---|
| **Course** | B.Sc. (Hons.) Computer Science — Research Methodology |
| **Submission Date** | 24 April 2026 |
| **Project Type** | Systematic Literature Review (secondary research) |
| **Authors** | Khushi Jain, Sanchi Goyal, Sanjana Singh |

> ⚠️ **This project does not include original experiments, model training, or
> deployment.** It is a review and synthesis of existing published research. See
> [Academic Disclaimer](#academic-disclaimer) below.

---

## Overview

Stock market prediction has long been one of the most studied — and most difficult —
problems in quantitative finance, given the noisy, non-stationary, and sentiment-driven
nature of price movements. This project reviews how AI/ML has been applied to this
problem, consolidating findings from 19 academic sources into a single, organized
synthesis. It examines the techniques used (classical ML, deep learning, ensembles,
and sentiment analysis), the data sources these studies drew on, how model performance
was measured and compared, and the recurring gaps and limitations across the field.

## Research Objectives

Based on the introduction and structure of the paper, the review sets out to:

1. Consolidate and organize existing AI/ML research on stock market prediction.
2. Identify which AI/ML techniques (classical ML, deep learning, ensemble/hybrid,
   sentiment-based) appear most frequently in the literature.
3. Examine what data sources and feature types (price history, technical indicators,
   fundamentals, sentiment/text) are used across studies.
4. Review how model performance is measured and compared across the literature.
5. Identify recurring research gaps and propose directions for future work.

## Research Methodology

This paper is a **narrative/thematic literature review** rather than a formally
protocolized systematic review. Based on what is present in the uploaded document:

- **What the paper does:** groups reviewed studies thematically (classical ML → deep
  learning → ensemble/hybrid → sentiment-based → meta-reviews), summarizes each
  study's technique, dataset, and reported results, and synthesizes recurring themes,
  gaps, and limitations across them.
- **What the paper does *not* document:** a PRISMA-style flow, explicit inclusion/exclusion
  criteria, named search databases (e.g., Scopus, IEEE Xplore, Web of Science), search
  strings/keywords used, or a stated date range for the search. These elements were not
  found anywhere in the uploaded paper.

**This is flagged honestly rather than assumed.** If you plan to publish or extend this
work formally, adding a documented search protocol (databases searched, search terms,
inclusion/exclusion criteria, and a PRISMA flow diagram of studies identified → screened
→ included) would substantially strengthen its methodological rigor. See
[Academic Improvements Needed](#academic-improvements-needed) for the full list.

## Topics / Techniques Reviewed

| Category | Techniques Covered |
|---|---|
| Classical Machine Learning | Logistic Regression, KNN, Decision Trees, Random Forest, SVM, Naïve Bayes |
| Deep Learning | Artificial Neural Networks (ANN), LSTM (incl. Deep LSTM, Stacked LSTM, Attention-based LSTM) |
| Ensemble & Hybrid Methods | Random Forest + XGBoost + LSTM ensembles, GA-SVM, GA-ANN, ARIMA hybrids |
| Sentiment / Multi-Source | Twitter/StockTwits sentiment, Word2Vec/N-Gram text encoding, news-based sentiment analysis |
| Theoretical Frameworks | Efficient Market Hypothesis (EMH), Adaptive Market Hypothesis (AMH) |

## Literature Review Summary

The review synthesizes 19 sources, organized into four thematic clusters plus a
meta-review of existing systematic reviews:

- **Classical ML** studies (e.g., Mokhtari et al.; Akhtar et al.; Sheth & Shah) generally
  report accuracies in the 75–93% range depending on technique and setup, with SVM and
  Random Forest performing consistently well on structured price/technical data.
- **Deep learning** studies show LSTM is widely adopted for its ability to retain
  long-range dependencies in sequential financial data, though results vary widely
  (~57–90%+ accuracy) depending on data volume and tuning.
- **Ensemble/hybrid** approaches (e.g., Sonkavde et al.'s RF+XGBoost+LSTM; Venkatarathnam
  et al.'s GA-SVM/GA-ANN) consistently outperformed standalone models in the studies
  that tested them.
- **Sentiment-based** studies show that incorporating text/sentiment data (Twitter,
  news) alongside price data tends to improve prediction accuracy, though sentiment
  classification itself remains only moderately accurate.
- A **meta-review** (Lin & Marques, 2024) synthesizing 10 prior reviews (379+ studies)
  found SVM, LSTM, and ANN to be the most commonly used methods overall, with historical
  price data as the dominant input (66% of studies) and *no* reviewed study combining
  sentiment + news + price + macroeconomic data simultaneously — identified as the key
  gap in the field.

Full study-by-study detail is in
[`Literature-Review/literature-review-table.xlsx`](Literature-Review/literature-review-table.xlsx).

## Comparative Analysis

The paper's own comparative table (Section 4) cross-references 16 of the reviewed
studies by technique, dataset, reported accuracy, contribution, and limitation. This
has been reproduced faithfully — with no fabricated values — in the spreadsheet above.
Where the source table's accuracy figures were ambiguous or not stated, this is marked
explicitly as **"Not specified"** rather than estimated.

## Key Findings

- No single AI/ML technique consistently outperforms all others across studies; results
  are highly dependent on the dataset, market, and time period tested.
- SVM, LSTM, and ANN are the most frequently used methods across the literature.
- Ensemble and hybrid methods (e.g., combining Random Forest, XGBoost, and LSTM) tend
  to outperform individual models where tested.
- Historical price data remains the dominant input, but studies incorporating sentiment
  or news data alongside price data tend to report improved accuracy.
- Data preprocessing and feature selection quality has a measurable impact on model
  performance across multiple studies.

## Research Gaps

The paper identifies eight recurring gaps across the reviewed literature:

1. **Limited use of diverse data types** — most studies rely on price/technical data alone; few combine technical, fundamental, and sentiment data together.
2. **Overfitting and poor generalizability** — models often perform well on training data but degrade on unseen periods, markets, or exchanges.
3. **Lack of standardized evaluation methods** — studies use inconsistent metrics (accuracy, F1, RMSE, MAE, R²) and inconsistent test datasets, making cross-study comparison difficult.
4. **Forecasting weakens over longer horizons** — most work targets short-term (next-day) prediction; long-term forecasting is underexplored.
5. **Limited research on emerging/non-Western markets** — most studies focus on the U.S., China, and Western Europe.
6. **Hybrid and ensemble methods still underexplored** relative to standalone models.
7. **Inadequate focus on transaction costs and realistic trading constraints.**
8. **Lack of model explainability/interpretability**, particularly for deep learning approaches (LSTM, CNN).

## Limitations

As stated or reasonably inferred from the paper itself:

- The review does not document a formal, replicable search methodology (see
  [Research Methodology](#research-methodology) above).
- Findings are a synthesis of *secondary* sources — no original data collection,
  model training, or empirical testing was performed as part of this project.
- Some source studies report accuracy figures that are not directly comparable
  (different markets, timeframes, and metrics), a limitation the review itself
  identifies as a field-wide issue (Research Gap #3) but which also applies to any
  synthesis drawn across them.
- The number of source studies (19) is modest for a claim of comprehensive coverage
  of a fast-moving field.

## Future Research Directions

As proposed in the paper's discussion (Section 5) and conclusion:

- Combining diverse data types (price, fundamentals, macroeconomic indicators, sentiment) within unified models.
- Extending prediction horizons beyond next-day/short-term forecasting.
- Expanding research coverage to emerging and non-Western markets (South Asia, Southeast Asia, Africa, Latin America).
- Developing more interpretable/explainable AI models for financial forecasting.
- Incorporating realistic trading constraints (transaction costs, liquidity, slippage) into model evaluation.
- Exploring novel data sources such as satellite imagery, web search trends, and corporate filings.

## Technologies / Concepts Covered

`Machine Learning` · `Deep Learning` · `LSTM` · `ANN` · `SVM` · `Random Forest` ·
`XGBoost` · `Ensemble Learning` · `Sentiment Analysis` · `NLP (Word2Vec, N-Gram)` ·
`Genetic Algorithms` · `ARIMA` · `Efficient Market Hypothesis` · `Adaptive Market Hypothesis`
· `Systematic Literature Review Methodology`

*(Note: these are the concepts **reviewed and discussed** in the paper — this project
did not implement code using these techniques. See [Future Extension](#future-extension-phase-2--not-yet-implemented) below.)*

## Project Structure

```
AI-Stock-Market-Prediction-Research/
│
├── README.md                                   → This file
│
├── Research-Paper/
│   ├── AI-in-Finance-Stock-Market-Prediction.pdf   → Full paper (typeset from LaTeX)
│   └── AI-in-Finance-Stock-Market-Prediction.tex   → LaTeX source (compiles clean, 0 errors)
│
├── Literature-Review/
│   └── literature-review-table.xlsx            → Structured summary of all 19 reviewed studies
│
├── References/
│   └── references.bib                          → BibTeX file of all 19 references
│
├── Reports/
│   └── plagiarism-and-ai-report.pdf             → Duplichecker + GPTZero originality reports
│
└── assets/
    └── images/                                  → Diagrams/figures (optional)
```

## References

19 sources are cited throughout the paper (numbered [1]–[19] in-text) spanning
2018–2024. The full list is provided in [`References/references.bib`](References/references.bib).
Notable sources include Mokhtari, Yen & Liu; Akhtar et al.; Sonkavde et al.; Sheth &
Shah; Bansal et al.; Khan et al.; Lin & Marques (meta-review); and Venkatarathnam et al.

> Note: the reference list gives Mokhtari, Yen & Liu as a 2018 publication, while the
> in-text discussion refers to it as a "2021 study" — this inconsistency exists in the
> source paper and should be reconciled against the original publication before formal use.

## Academic Disclaimer

This repository documents a **literature review / research methodology project**, not
an implemented, trained, or deployed AI/ML system. Specifically:

- No stock market prediction model was built, trained, or tested by the authors as part
  of this project.
- No proprietary dataset was collected; all data references are to datasets used in the
  *reviewed* third-party studies, not data used directly by this project.
- All accuracy/performance figures cited in this repository are as **reported by the
  original authors** of the reviewed studies, not results produced by this project.
- This project's contribution is the **synthesis, organization, and critical analysis**
  of existing published research.

## Author / Student Information

| Name | Roll No. | Course |
|---|---|---|
| Khushi Jain | 2023317 | B.Sc. (Hons.) Computer Science |
| Sanchi Goyal | 2023334 | B.Sc. (Hons.) Computer Science |
| Sanjana Singh | 2023337 | B.Sc. (Hons.) Computer Science |

---

## Future Extension (Phase 2 — Not Yet Implemented)

This literature review naturally motivates a follow-up **implementation project**. The
following is a proposed roadmap only — **none of it has been built as part of this
repository**:

- [ ] Collect historical stock price data (e.g., via Yahoo Finance API) for a defined set of tickers
- [ ] Perform data preprocessing and feature engineering (technical indicators, normalization)
- [ ] Implement baseline ML models (Logistic Regression, Random Forest, SVM)
- [ ] Implement deep learning models (LSTM, and/or a Transformer/Attention-based variant)
- [ ] Add a sentiment analysis pipeline (news/Twitter data + NLP embeddings)
- [ ] Build an ensemble model combining price-based and sentiment-based predictions
- [ ] Evaluate using standardized, pre-registered metrics (accuracy, RMSE, MAE, R²) on a held-out test period
- [ ] Build a simple dashboard to visualize predictions vs. actuals

---

*This README was reorganized and polished for GitHub presentation from the original
academic submission. All research content, findings, and conclusions are drawn directly
from the uploaded paper; no claims, results, or techniques have been added beyond what
the source document contains.*
