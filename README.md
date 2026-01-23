# Predicting Social Unrest Using Lagged Economic Indicators
## A Time Series Machine Learning Early Warning System

---

## Executive Summary

This project develops a forward looking time series machine learning system to anticipate elevated and high risk social unrest conditions using lagged macroeconomic indicators.

Rather than explaining past unrest, the model is explicitly designed for **early warning**, enabling policymakers, analysts, and researchers to identify mounting structural stress before visible unrest emerges.

The system prioritizes recall to minimize missed risk signals, making it suitable for real world monitoring and decision support contexts.

---

## Key Results

- **F1 Score:** 0.88  
- **Recall:** 0.99  
- **Objective:** Early detection of elevated and high risk unrest regimes  

High recall ensures that emerging unrest signals are rarely missed, which is critical in prevention and preparedness settings.

---

## Problem Framing

Social unrest does not arise from isolated shocks. It emerges from the accumulation of unresolved economic pressure over time.

Traditional models often fail by relying on contemporaneous indicators or retrospective correlations. This project reframes unrest prediction as a **temporal risk accumulation problem**, where lagged economic stressors provide stronger predictive signal than point in time values.

---

## Data Engineering Philosophy

### The Pressure Cooker Effect

Economic stress compounds gradually rather than instantaneously.

Lagged features capture delayed mechanisms such as:

- Unemployment driven household instability  
- Real income erosion and declining purchasing power  
- Savings depletion and debt accumulation over multi month horizons  
- Psychological and behavioral stress delays  

Lag windows of approximately 180 days are engineered to transform raw indicators into measures of structural tension.

---

## Modeling Approach

- Chronologically ordered feature engineering to prevent data leakage  
- Time series aware train test splits  
- Classification framing aligned to actionable risk thresholds  
- Recall prioritized to minimize missed unrest signals  

The model is intentionally conservative, favoring early warnings over late confirmations.

---

## Validation Strategy

Random train test splits are inappropriate for time series prediction and lead to information leakage.

This project uses **chronological splits** and **time series cross validation** to ensure that all predictions are made strictly forward in time, mirroring real deployment conditions.

---

## Interpretability and Risk Use

This system is designed as a **decision support tool**, not a deterministic forecast engine.

Model outputs should be interpreted as:

- Elevated probability of unrest conditions  
- Signals of mounting economic pressure  
- Triggers for deeper qualitative or policy analysis  

The model does not predict specific events, actors, or locations. It flags systemic risk environments.

---

## Visualization

Engineered features and predictions are exported for Tableau to support:

- Time series inspection of stress buildup  
- Regime shifts between low and high risk periods  
- Executive level dashboards for non technical stakeholders  

---

## Limitations

- Macroeconomic indicators cannot capture all sociopolitical catalysts  
- Reporting delays introduce latency  
- Structural dynamics vary across regions  

These limitations reinforce the model’s role as an early warning complement rather than a standalone predictor.

---

## Ethical Considerations

- No individual level data is used  
- No surveillance or personal monitoring  
- Outputs are probabilistic and aggregated  

The system is designed to support prevention and resilience planning rather than enforcement.

---

## Conclusion

Lagged economic indicators provide powerful early warning signals for social unrest risk.

By reframing unrest as a time dependent accumulation process, this project moves beyond retrospective analysis toward actionable foresight, demonstrating how machine learning can be responsibly applied to complex social systems.

---

## Future Extensions

- SHAP based temporal interpretability  
- Regime detection using hidden Markov models  
- Cross country generalization testing  
- Integration of non economic stress indicators  

