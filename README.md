# U.S. Mortality Prediction — Multi-Method ML Study

A machine learning study predicting all-cause mortality in the U.S. using classification, regression, and clustering across individual- and population-level data.

**Team:** David Ahn · Yinghui Chen · Travis Robinson

---

## Setup

```bash
git clone https://github.com/helenachen03/mortality-rate-prediction.git
cd mortality-rate-prediction
pip install -r requirements.txt
```

---

## Data
- **NHANES** — individual health exams and lab values (29,986 records, 1999–2017)
- **CDC WONDER** — population-level mortality rates (4,488 records, 1999–2020)
- **National Death Index** — individual mortality outcomes linked to NHANES (101,316 records)

## Methods & Results

| Task | Best Model | Key Metric |
|---|---|---|
| Classification (10-yr survival) | Gradient Boosted Tree | ROC AUC: best in class, F1: 0.92 |
| Regression (mortality count) | Random Forest | R²: 0.993, RMSE: 115.4 |
| Clustering (population profiles) | K-Means / Hierarchical | k = 3 clusters |

**Consistent finding across all methods: age is the dominant predictor of mortality.** Gender and health indicators had comparatively modest impact.

## Clusters
Three population health profiles emerged: younger/healthy (lowest mortality), older females with moderate cardiometabolic risk (intermediate), and older males with elevated cardiometabolic burden (highest mortality).

## References
- Levantesi & Pizzorusso (2019) — [doi.org/10.3390/risks7010026](https://doi.org/10.3390/risks7010026)
- Qiu et al. (2022) — [doi.org/10.1038/s43856-022-00180-x](https://doi.org/10.1038/s43856-022-00180-x)
- Williams et al. (2020) — [amstat.org](https://ww2.amstat.org/meetings/proceedings/2020/data/assets/pdf/1505462.pdf)