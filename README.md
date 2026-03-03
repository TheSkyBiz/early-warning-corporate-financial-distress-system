# Early Warning Corporate Financial Distress System

## End-to-End Bankruptcy Risk Modeling Across 1--5 Year Horizons

------------------------------------------------------------------------

## Project Overview

This project develops a multi-horizon corporate bankruptcy early-warning
system using classical financial ratios, linear models, and nonlinear
ensemble learning.

The study evaluates predictive performance across 1--5 year forecast
horizons and incorporates decision-theoretic threshold optimization
under asymmetric financial loss.

**Dataset Summary:** - 5 separate bankruptcy datasets (1year--5year) -
Total firms analyzed: \~43,405 - Bankruptcy rate range: 3.86% → 6.94% -
64 engineered financial ratios per firm

------------------------------------------------------------------------

# Project Structure

    early-warning-corporate-financial-distress-system/
    │
    ├── data/
    │ └── raw/ # Original ARFF bankruptcy datasets (1–5 year)
    │
    ├── notebooks/
    │ 01_data_understanding.ipynb
    │ 02_logistic_baseline.ipynb
    │ 03_tree_models.ipynb
    │ 04_altman_benchmark.ipynb
    │ 05_horizon_decay_analysis.ipynb
    │ 06_cost_sensitive_analysis.ipynb
    │ 07_feature_stability_analysis.ipynb
    │
    ├── results/ # Exported high-resolution figures
    │ horizon_roc_curve.png
    │ threshold_vs_horizon.png
    │ min_loss_vs_horizon.png
    │ threshold_sensitivity.png
    │ feature_stability_overlap.png
    │
    ├── requirements.txt # Python dependencies for reproducibility
    │
    ├── .gitignore
    │
    └── README.md

------------------------------------------------------------------------

# Environment & Setup

## 1️⃣ Clone Repository

``` bash
git clone https://github.com/TheSkyBiz/early-warning-corporate-financial-distress-system
cd early-warning-corporate-financial-distress-system
```

## 2️⃣ Create Virtual Environment (Recommended)

``` bash
python -m venv venv
source venv/bin/activate        # macOS/Linux
venv\Scripts\activate         # Windows
```

## 3️⃣ Install Dependencies

``` bash
pip install -r requirements.txt
```

------------------------------------------------------------------------

# ▶️ Reproducibility Instructions

To fully reproduce results:

1.  Place ARFF files inside `data/raw/`
2.  Run notebooks in order:

-   01_data_understanding
-   02_logistic_baseline
-   03_tree_models
-   04_altman_benchmark
-   05_horizon_decay_analysis
-   06_cost_sensitive_analysis
-   07_feature_stability_analysis

For strict reproducibility:

Use `Kernel → Restart & Run All` in each notebook.

All major plots are automatically saved to `/results` at 300 DPI
resolution.

------------------------------------------------------------------------

# Key Results Snapshot

-   Classical Altman-style model: ROC-AUC ≈ 0.71
-   Logistic regression (L1): ROC-AUC ≈ 0.75
-   XGBoost (1-year): ROC-AUC ≈ 0.97
-   Optimal thresholds range: 0.099 → 0.386 depending on horizon
-   Bankruptcy prevalence increases from 3.86% → 6.94% across horizons

------------------------------------------------------------------------

# Core Contributions

-   Demonstrated nonlinear dominance in financial distress prediction.
-   Identified temporal regime shifts across forecast horizons.
-   Implemented cost-sensitive threshold optimization aligned with risk
    appetite.
-   Verified structural stability of financial fragility indicators
    across time.

------------------------------------------------------------------------

# Final Takeaway

This project bridges:

Financial theory → Linear modeling → Nonlinear ensemble learning →
Temporal regime analysis → Deployment-aware cost optimization.

It demonstrates full-stack applied machine learning in a real-world risk
modeling context.
