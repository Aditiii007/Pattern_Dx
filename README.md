# PatternDx — Pattern-Based Diagnostic System for Student Struggle in Online Learning

**CS907 MSc Dissertation | University of Warwick | u5734711**  
Supervisor: Prof. Long Tran-Thanh

---

## Project Overview

PatternDx is a prescriptive analytics system that identifies distinct modes of student struggle in online learning and connects them to evidence-based intervention guidance. Unlike binary early warning systems that produce undifferentiated at-risk flags, PatternDx diagnoses *which* pattern of struggle a student exhibits and recommends targeted support.

**Live prototype:** https://aditiii007.github.io/Pattern_Dx/

---

## Key Results (from OULAD, n=32,593 students)

| Metric | Value |
|--------|-------|
| Patterns discovered | 6 (K-means, HDBSCAN, GMM all converge) |
| Silhouette score | 0.297 |
| Chi-square (outcome × pattern) | 13,489.3, p < 0.001 |
| Best classifier | XGBoost, 0.710 macro-F1 @ week 4 |
| Random Forest macro-F1 @ week 4 | 0.686 |
| Ghost pattern fail/withdraw rate | 76.4% |
| High Achiever fail/withdraw rate | 6.1% |
| Instructor preference for PatternDx | 4/4 (100%) |

**Six patterns:** High Achiever, Steady Worker, Procrastinator, Conceptual Struggler, Disengaging, Ghost

---

## Repository Contents

| File | Description |
|------|-------------|
| `index.html` | PatternDx browser prototype — open in any browser, offline, no dependencies |
| `PatternDx_Pipeline.ipynb` | Full ML pipeline: data download, feature engineering, clustering, classification, SHAP, intervention mapping |
| `requirements.txt` | Python dependencies |
| `README.md` | This file |

---

## Running the Pipeline

### Option A — Google Colab (recommended)
1. Open [colab.research.google.com](https://colab.research.google.com)
2. File → Open notebook → GitHub → paste this repo URL
3. Select `PatternDx_Pipeline.ipynb`
4. Runtime → Run all (~15 min)

### Option B — Local
```bash
pip install -r requirements.txt
jupyter notebook PatternDx_Pipeline.ipynb
```

OULAD data (~50 MB) downloads automatically from the UCI Machine Learning Repository when you run the notebook.

---

## PatternDx Prototype

Open `index.html` in any browser. No server, no API, no internet connection required.

Features:
- 10 student profiles covering all 6 patterns
- Diagnosis, Interventions, Prognosis, and Feature Importance tabs per student
- Compare mode — select two students for side-by-side analysis
- SHAP-informed feature weights derived from actual OULAD pipeline run

---

## Dataset

**OULAD** — Open University Learning Analytics Dataset  
Kuzilek, J., Hlosta, M., & Zdrahal, Z. (2017). *Open University Learning Analytics Dataset*. Scientific Data, 4, 170171.  
Available at: https://analyse.kmi.open.ac.uk/open_dataset  
Licence: Creative Commons Attribution 4.0

---

## Citation

If you use this work, please cite:

> Sharma, A. (2026). *PatternDx: A Pattern-Based Diagnostic System for Student Struggle in Online Learning*. MSc Dissertation, University of Warwick.
