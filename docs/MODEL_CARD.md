# KlaimNexus v0.7.1 — Prototype Model Card

## Intended use

KlaimNexus is designed as an **AI-assisted claim investigation and review-prioritization prototype** for identifying claim pairs that may deserve additional human review, especially patterns related to repeat billing and claim cloning.

It is **not** intended to:

- automatically determine that fraud has occurred;
- reject claims automatically;
- replace medical, audit, or verifier judgement;
- be treated as a production BPJS Kesehatan model.

## Evaluation data

The current evaluation is based on **synthetic/anonymized prototype data**, not real JKN participant data.

Prototype scenarios include difficult legitimate cases such as clinical look-alikes and legitimate readmissions, alongside synthetic suspicious patterns such as exact repeat, modified repeat, partial clone, date-shift clone, amount-modified clone, and semantic clone.

## Internal evaluation snapshot

| Metric | Prototype result |
|---|---:|
| PR-AUC | 0.7766 |
| Hard-positive AP | 0.5766 |
| P3 Precision | 88.48% |
| P3 Recall | 51.68% |
| P3 Hard-positive Recall | 31.64% |
| Clinical look-alike FPR (P3) | 4.36% |
| Legitimate readmission FPR (P3) | 3.64% |

### P3 recall by synthetic pattern

| Pattern | Recall |
|---|---:|
| Exact Repeat | 93.1% |
| Modified Repeat | 89.2% |
| Partial Clone | 36.6% |
| Amount Modified | 40.3% |
| Date Shift | 20.4% |
| Semantic Clone | 27.3% |

Three-seed PR-AUC values were approximately **0.7594 / 0.7676 / 0.7590** with standard deviation around **0.004**.

## Interpretation

The prototype performs more strongly on explicit repeat patterns and remains more challenging on subtle cloning patterns. This is why KlaimNexus is positioned around **review prioritization + explainability**, not autonomous claim adjudication.

## Known limitations

- Evaluation uses synthetic prototype data; external validity must be tested with authorized real-world data.
- Subtle clone recall remains an improvement area.
- Thresholds require domain validation and calibration before real deployment.
- Dataset representativeness, concept drift, and false-positive/false-negative behavior require ongoing monitoring.
- Production-grade raw-claim-to-model inference integration and operational validation remain roadmap items.

## Governance principle

**AI provides priority, similarity, pattern, evidence and context. Human reviewers make the final decision.**
