# Kaggle work log

Short dated notes on what I tried and what happened. Scores are real leaderboard results.

## 2026-11-05
- **Google Quantum AI (verifiable circuit compilation):** credited copy of a public refit scored **24.594** (up from 23.172).
- **Enveda CASMI 2026:** credited copy of a public neural ensemble scored **0.480** (up from 0.476).
- **Squares in Squares:** credited copy of a public LP refinement scored **22.2540** (down from 22.2603; lower is better).
- Running next: public 24.80 (Quantum) and 0.672 (Name That LLM) versions.

## 2026-11-03
- **Name That LLM:** the credited 0.666 copy scored **0.666** public LB (up from 0.662).
- **Playground S6E11:** public notebooks now reach 0.9522 with GLM + boosting stacks and "digit" features on the generated numbers.

## 2026-11-02
- **Name That LLM:** submitted a credited copy of a 0.666 public notebook (previous best 0.662). Score pending.
- **Playground S6E11 (fraud):** LightGBM baseline scored **0.94664** public LB (CV 0.94619). Top of the LB is ~0.952.
  Public notebooks reach ~0.951 with "digit" features on the generated numbers; that is the next thing to test.

## 2026-11-01
- **Playground S6E11:** published [Synthetic vs original: does it help?](s6e11-fraud-synthetic-vs-original/).
  Original data is easy to tell apart (adversarial AUC 0.90) and adding it does not help (-0.00016 CV AUC).

## 2026-10-31
- **Gemma 4 Developer Agent:** published [Where is the bug?](gemma4-where-is-the-bug/).
  Hybrid search finds the right file in the top 5 for 68% of 128 tasks; graph-node BM25 reaches 84% in the top 10.
