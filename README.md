# Telecom AI/ML Portfolio

> **Portfolio Project**: Demonstrating AI/ML application to real-world telecom challenges using domain expertise from 10+ years in network operations.

[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![uv](https://img.shields.io/badge/managed%20by-uv-blue)](https://github.com/astral-sh/uv)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## Projects

| # | Project | ML Type | Algorithm | Target | Result |
|:---:|:---|:---|:---|:---|:---|
| 1 | [Churn Prediction](https://github.com/adityonugrohoid/telecom-churn-prediction) | Binary Classification | XGBoost | `is_churned` | AUROC: 0.86 |
| 2 | [Root Cause Analysis](https://github.com/adityonugrohoid/telecom-root-cause-analysis) | Multi-class Classification | XGBoost | `is_root_cause` | Acc@3: 1.00 |
| 3 | [Anomaly Detection](https://github.com/adityonugrohoid/telecom-anomaly-detection) | Unsupervised | Isolation Forest | `label_anomaly` | F1: 0.70 |
| 4 | [QoE Prediction](https://github.com/adityonugrohoid/telecom-qoe-prediction) | Regression | LightGBM | `mos_score` | RMSE: 0.04 |
| 5 | [Capacity Forecasting](https://github.com/adityonugrohoid/telecom-capacity-forecasting) | Time-Series | LightGBM+Prophet | `traffic_load_gb` | MAPE: 1.6% |
| 6 | [Network Optimization](https://github.com/adityonugrohoid/telecom-network-optimization) | Reinforcement Learning | Q-Learning | KPI improvement | +61% vs random |

---

## What This Portfolio Demonstrates

- **Domain Expertise**: Deep understanding of telecom network operations and challenges
- **Problem Framing**: Translating business problems into well-defined ML tasks
- **Data Engineering**: Hand-crafted synthetic data generators with embedded telecom physics
- **End-to-End Thinking**: Data generation, feature engineering, modeling, evaluation, and business insights
- **Communication**: Clear documentation for both technical and business audiences

---

## Technology Stack

| Category | Tools |
|:---|:---|
| Language | Python 3.11+ |
| Package Manager | [uv](https://github.com/astral-sh/uv) |
| ML Frameworks | XGBoost, LightGBM, scikit-learn |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Interpretability | SHAP |
| Testing | pytest |
| Linting | Ruff |
| CI/CD | GitHub Actions |

---

## Quick Start

Each project is fully independent. To explore one:

```bash
cd 01-churn-prediction
uv sync
uv run python -m churn_prediction.data_generator
uv run jupyter lab notebooks/
```

See each project's `QUICKSTART.md` for detailed instructions.

---

## Project Structure

Every project follows the same structure:

```
0X-project-name/
├── .github/workflows/ci.yml    # CI pipeline
├── data/
│   ├── raw/                    # Generated synthetic data
│   └── processed/              # Feature-engineered datasets
├── src/{package_name}/
│   ├── __init__.py             # Package exports
│   ├── config.py               # Configuration management
│   ├── data_generator.py       # Domain-informed data generation
│   ├── features.py             # Feature engineering pipeline
│   └── models.py               # ML model implementations
├── notebooks/
│   └── 0X_analysis.ipynb       # Main analysis notebook
├── tests/
│   └── test_data_quality.py    # Data quality tests
├── .gitignore
├── pyproject.toml
├── README.md
├── QUICKSTART.md
└── CONTRIBUTING.md
```

---

## Author

**Adityo Nugroho**
Telecom Professional | AI/ML Practitioner

---

## License

All projects are MIT licensed for educational and portfolio purposes.
