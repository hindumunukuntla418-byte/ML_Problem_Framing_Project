# Risk Register

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Data leakage | Medium | High | Only use information available at the decision point |
| Missing data | Medium | Medium | Check missing values and send incomplete cases for review |
| False negatives | Medium | High | Monitor recall and allow human review |
| False positives | Medium | Medium | Monitor precision and advisor workload |
| Dataset bias | Medium | High | Evaluate data quality and population coverage |
| Model drift | Medium | Medium | Monitor performance over time |
| Privacy risk | Low for synthetic data | High for real data | Use privacy controls and authorized access |
| Automation misuse | Medium | High | Require human review |
| Poor data quality | Medium | High | Validate input data before prediction |
| Unexpected model behavior | Low | High | Monitoring and rollback process |

## Rollback Conditions

The model should be stopped if:

1. Serious data leakage is discovered.
2. Input data becomes unreliable.
3. Model performance becomes unacceptable.
4. A significant privacy issue is discovered.
5. Unsafe or unexpected predictions are identified.
6. Human reviewers determine that the system is causing harmful decisions.