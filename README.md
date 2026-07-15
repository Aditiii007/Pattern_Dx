# PatternDx: CS907 Dissertation Preliminary Code
**Aditi Sharma | MSc Data Analytics | University of Warwick | July 2026**
Supervisor: Prof. Long Tran-Thanh

## Files

### PatternDx_Pipeline.ipynb
Full ML pipeline notebook covering all four research phases:
- Phase 1: Feature engineering (45 features, 3 time cutoffs)
- Phase 2: Pattern discovery (K-means, HDBSCAN, GMM)
- Phase 3: Early classification (RF, XGBoost, LR + SHAP)
- Phase 4: Intervention mapping and validation

OULAD data (~200MB) is downloaded automatically when the 
notebook is run, no manual download required.

### index.html
PatternDx browser-based diagnostic prototype. Open in any 
browser. Runs entirely offline, no internet or login required.

## How to run the notebook

1. Install dependencies:
   pip install -r requirements.txt

2. Launch Jupyter:
   jupyter notebook

3. Open PatternDx_Pipeline.ipynb and run all cells.
   Runtime: approximately 15-20 minutes on CPU.

## Data
OULAD (Open University Learning Analytics Dataset) is 
downloaded automatically from the public GitHub mirror 
of the original release (Kuzilek et al., 2017, 
doi:10.1038/sdata.2017.171). No data files are included 
in this ZIP as they are publicly available and 
auto-downloaded by the notebook.
