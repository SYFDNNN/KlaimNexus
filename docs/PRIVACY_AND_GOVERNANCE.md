# Privacy, Safety & Governance

KlaimNexus is designed as a decision-support prototype for claim investigation. The current portfolio materials use synthetic/anonymized data and do not contain real JKN participant data.

## Data principles

- Data minimization
- Anonymization / pseudonymization for authorized future use
- Role-based access for production environments
- Encryption in transit and at rest for production deployments
- Audit trail for reviewer actions
- Clear separation between model signal and human decision

## AI risks considered

- False positives
- False negatives
- Dataset bias / representativeness
- Concept drift
- Threshold instability
- Overreliance on automated scores

## Mitigation roadmap

- Human-in-the-loop review
- Explainable similarity breakdowns and detected signals
- Threshold calibration with domain experts
- Periodic evaluation
- Model monitoring
- Verifier feedback loop
- Controlled pilot before production deployment

## Decision boundary

A priority tier such as **P1, P2, or P3 is not a fraud verdict**. It indicates review priority only.
