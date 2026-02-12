# Telecom ML Portfolio — Standards & Conventions

## Version Pins (SHAP Compatibility)
- `numpy>=1.24.0,<2.0` — SHAP color conversion bug with NumPy 2.x
- `xgboost>=1.7.0,<2.0` — SHAP incompatible with XGBoost 2.x base_score
- `shap>=0.42.0`
- `numba>=0.59.0` — Python 3.12 support
- `pandas>=2.1.0`, `scikit-learn>=1.3.0`, `lightgbm>=4.1.0`
- `matplotlib>=3.8.0`, `seaborn>=0.13.0`
- `jupyter>=1.0.0`, `tqdm>=4.66.0`, `pyyaml>=6.0`
- Dev: `pytest>=7.4.0`, `pytest-cov>=4.1.0`, `ruff>=0.1.0`

## Seaborn Cell 1 (Identical in every notebook)
```python
import warnings
warnings.filterwarnings("ignore")

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

sns.set_context("notebook")
sns.set_style("whitegrid")
sns.set_palette("husl")

plt.rcParams['figure.figsize'] = (12, 6)
plt.rcParams['figure.dpi'] = 100
```

## Naming Conventions
- Dir: `0X-kebab-case/`
- Package: `snake_case` (under `src/`)
- Repo: `telecom-kebab-case`
- Notebook: `0X_snake_case.ipynb`

## Commit Style
- `feat: initial project — {description}`
- Conventional commits: `feat:`, `fix:`, `docs:`, `test:`, `chore:`

## Project Structure (Every project)
```
0X-project-name/
├── .github/workflows/ci.yml
├── data/raw/ & data/processed/
├── src/{package_name}/
│   ├── __init__.py
│   ├── config.py
│   ├── data_generator.py
│   ├── features.py
│   └── models.py
├── notebooks/0X_name.ipynb
├── tests/test_data_quality.py
├── docs/
├── .gitignore
├── pyproject.toml
├── README.md
├── QUICKSTART.md
└── CONTRIBUTING.md
```

## Notebook Structure (8 sections, every notebook)
1. Setup & Configuration
2. Data Loading & Validation
3. Exploratory Data Analysis
4. Feature Engineering
5. Model Training
6. Evaluation & Metrics
7. Interpretation (SHAP where applicable)
8. Business Insights & Conclusions

## Tool Config (Identical in all pyproject.toml)
- `requires-python = ">=3.11"`
- ruff: `line-length = 100`, `target-version = "py311"`
- pytest: `testpaths = ["tests"]`, `addopts = "-v --tb=short"`
