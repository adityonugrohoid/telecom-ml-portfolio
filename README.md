<div align="center">

# Telecom ML Portfolio

[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**Six end-to-end telecom ML projects: churn, anomaly detection, QoE, forecasting, and network optimization**

[Projects](#projects) | [Related Projects](#related-projects)

</div>

---

## Table of Contents

- [The Problem](#the-problem)
- [Projects](#projects)
- [Project Structure](#project-structure)
- [Related Projects](#related-projects)
- [License](#license)
- [Author](#author)

## The Problem

### Telecom Operations at Scale

Network operations teams generate continuous streams of KPI data across thousands of cell sites, but most ML demonstrations treat telecom as interchangeable with generic tabular data. Reproducing realistic behavior (temporal correlation, spatial clustering, equipment failure signatures) requires domain-specific data generation, not public datasets.

### The Solution

Each project in this portfolio hand-crafts synthetic data with embedded telecom physics, then applies the appropriate ML paradigm end-to-end: from data generation through feature engineering, model training, evaluation, and business insight translation. Results are traceable and reproducible within each child repo.

## Projects

| # | Project | ML Type | Algorithm | Target | Result |
|:---:|:---|:---|:---|:---|:---|
| 1 | [Churn Prediction](https://github.com/adityonugrohoid/telecom-churn-prediction) | Binary Classification | XGBoost | `is_churned` | AUROC: 0.86 |
| 2 | [Root Cause Analysis](https://github.com/adityonugrohoid/telecom-root-cause-analysis) | Multi-class Classification | XGBoost | `is_root_cause` | Acc@1: 0.91 |
| 3 | [Anomaly Detection](https://github.com/adityonugrohoid/telecom-anomaly-detection) | Unsupervised | Isolation Forest | `label_anomaly` | F1: 0.70 |
| 4 | [QoE Prediction](https://github.com/adityonugrohoid/telecom-qoe-prediction) | Regression | LightGBM | `mos_score` | RMSE: 0.45 |
| 5 | [Capacity Forecasting](https://github.com/adityonugrohoid/telecom-capacity-forecasting) | Time-Series | LightGBM + Prophet | `traffic_load_gb` | MAPE: 14.5% |
| 6 | [Network Optimization](https://github.com/adityonugrohoid/telecom-network-optimization) | Reinforcement Learning | Q-Learning | KPI improvement | +61% vs random |

Each project is self-contained with its own dependencies, notebooks, and quickstart guide.

## Project Structure

This repo is an index. All source code, notebooks, and tests live in the six child repos linked above.

## Related Projects

| Project | Description |
|---------|-------------|
| [telecom-ml-framework](https://github.com/adityonugrohoid/telecom-ml-framework) | Spec-first ML project templates and domain-informed data generators for 6 telecom use cases |
| [telecom-churn-prediction](https://github.com/adityonugrohoid/telecom-churn-prediction) | Binary classification predicting subscriber churn (XGBoost, AUROC 0.86) |
| [telecom-root-cause-analysis](https://github.com/adityonugrohoid/telecom-root-cause-analysis) | Multi-class ranking of root causes in alarm cascades (XGBoost, Acc@1 0.91) |
| [telecom-anomaly-detection](https://github.com/adityonugrohoid/telecom-anomaly-detection) | Unsupervised cell-level anomaly detection on KPI time-series (Isolation Forest, F1 0.70) |
| [telecom-qoe-prediction](https://github.com/adityonugrohoid/telecom-qoe-prediction) | Session-level MOS regression from network KPIs (LightGBM, RMSE 0.45) |
| [telecom-capacity-forecasting](https://github.com/adityonugrohoid/telecom-capacity-forecasting) | Hourly per-cell traffic forecasting (LightGBM, MAPE 14.5%) |
| [telecom-network-optimization](https://github.com/adityonugrohoid/telecom-network-optimization) | RL-based RAN parameter tuning (Q-Learning, +61% vs random) |

## License

This project is licensed under the [MIT License](LICENSE).

## Author

**Adityo Nugroho** ([@adityonugrohoid](https://github.com/adityonugrohoid))
