# Predicting Social Unrest Using Lagged Economic Indicators
## A Time Series Machine Learning Early Warning System

---

## Executive Summary

This project develops a forward looking time series machine learning system to anticipate elevated and high risk social unrest conditions using lagged macroeconomic indicators.

Rather than explaining past unrest, the model is explicitly designed for early warning. The goal is to surface mounting structural stress before visible unrest emerges, enabling policymakers, analysts, and researchers to respond proactively.

The system prioritizes recall to minimize missed risk signals, making it appropriate for real world monitoring and prevention oriented decision support.

---

## Key Results

- F1 Score: 0.88  
- Recall: 0.99  
- Objective: Early detection of elevated and high risk unrest regimes  

High recall ensures that emerging unrest signals are rarely missed, which is critical in preparedness and mitigation contexts.

---

## Problem Framing

Social unrest does not arise from isolated shocks. It emerges from the accumulation of unresolved economic pressure over time.

Many traditional approaches rely on contemporaneous indicators or retrospective correlations. These methods often fail in real deployments because they do not capture delayed behavioral and structural effects.

This project reframes unrest prediction as a time dependent risk accumulation problem, where lagged economic stressors provide stronger and more actionable signal than point in time values.

---

## Data Engineering Philosophy

### The Pressure Cooker Effect

Economic stress compounds gradually rather than instantaneously.

Lagged features are engineered to capture delayed mechanisms such as:

- Unemployment driven household instability  
- Real income erosion and declining purchasing power  
- Savings depletion and debt accumulation across multi month horizons  
- Psychological and behavioral stress delays  

Lag windows of approximately 180 days transform raw indicators into measures of structural tension rather than short term volatility.

---

## Modeling Approach

- Chronologically ordered feature engineering to prevent information leakage  
- Time series aware train test splits  
- Classification framing aligned to actionable risk thresholds  
- Recall prioritized to reduce the probability of missed unrest signals  

The model is intentionally conservative. It favors early warnings over late confirmations.

---

## Validation Strategy

Random train test splits are inappropriate for time dependent systems and introduce forward looking bias.

This project uses chronological splits and time series cross validation to ensure that all predictions are generated strictly forward in time, mirroring real deployment conditions.

---

## Interpretability

Model interpretability is essential for trust and responsible use.

SHAP based feature attribution is used to:

- Identify which lagged indicators contribute most to elevated risk predictions  
- Verify alignment between model behavior and economic theory  
- Detect potential spurious correlations  

Interpretability analysis confirms that long horizon economic pressure variables dominate short term noise, reinforcing the pressure accumulation hypothesis.

---

## Risk Interpretation and Use

This system is designed as a decision support tool rather than a deterministic forecast engine.

Model outputs should be interpreted as:

- Elevated probability of unrest conditions  
- Signals of mounting economic pressure  
- Triggers for deeper qualitative, political, or policy analysis  

The model does not predict specific events, actors, or locations. It flags systemic risk environments.

---

## Visualization

Engineered features and predictions are exported for Tableau visualization to support:

- Time series inspection of economic stress buildup  
- Regime transitions between low and high risk periods  
- Executive level dashboards for non technical stakeholders  

---

## Model Governance

Responsible deployment requires explicit governance considerations.

Key principles include:

- High recall is prioritized intentionally, accepting higher false positives to avoid missed risk signals  
- Outputs should inform planning and prevention rather than enforcement  
- Predictions sh
