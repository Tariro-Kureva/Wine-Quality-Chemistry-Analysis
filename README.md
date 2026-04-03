# 🍷 What Makes a Great Wine?
### Uncovering the Chemistry Behind Quality Ratings using PCA & Dimensionality Reduction

> *Sommeliers taste it. Chemists measure it. Data scientists explain it.*

**Author:** Tariro Kureva | BAN 628 — Group Lab Project | February 2026

---

## 💡 The Business Problem
A wine producer has 11 chemical variables to track per bottle — acidity, sulfur dioxide, alcohol, pH, density and more. Which ones actually matter for quality? Which ones are just noise? And can a winemaker use chemistry alone to predict whether a batch will score well before it ever reaches a sommelier?

This project uses **Principal Component Analysis (PCA)** to cut through the complexity and find the chemical fingerprint of a great wine.

---

## 💥 Key Stats

| Stat | Value |
|------|-------|
| 🍾 Wine samples analyzed | 1,143 red wines |
| 🧪 Chemical features | 11 physicochemical properties |
| 🎯 Target | Quality score (0–10) by expert sommeliers |
| 📉 Dimensions after PCA | 7 principal components (from 11) |
| 🏆 Strongest quality driver | Alcohol (+0.48 correlation) |
| ⚠️ Biggest quality detractor | Volatile acidity (−0.39 correlation) |
| 📐 PCA criterion | Kaiser's rule (eigenvalue > 1) |

---

## 🔑 Key Findings

### 1. Two chemicals dominate quality — alcohol and volatile acidity
Alcohol (+0.48) is the single strongest positive predictor of quality. Volatile acidity (−0.39) is the biggest detractor. Everything else is secondary. If you want a better wine — ferment longer and control your acidity.

### 2. 11 features → 7 dimensions, most variance retained
Using Kaiser's criterion (eigenvalue > 1), PCA reduced 11 correlated chemical features to 7 independent principal components — simplifying the analysis without losing the majority of information.

### 3. Each component maps to a real winemaking concept
The PCA didn't just reduce numbers — it revealed meaningful chemical profiles that winemakers already understand:

| Component | Interpretation | Key Features |
|-----------|---------------|--------------|
| PC1 | Acidity Profile | Fixed acidity, citric acid, pH, density |
| PC2 | Alcohol & Quality | Alcohol, volatile acidity, quality |
| PC3 | Sulfur Dioxide Intensity | Free & total SO₂ |
| PC4 | Chlorides & Sweetness | Chlorides, residual sugar |
| PC5 | Sugar & Sulphates | Residual sugar, sulphates |

### 4. Fixed acidity, citric acid and density move together
These three variables cluster tightly in the correlation matrix — confirming that acidity management is a single production lever, not three separate ones.

---

## 🧪 The Chemistry of Quality

```
Higher quality wines tend to have:
✅ Higher alcohol content (target 11–13%)
✅ Lower volatile acidity
✅ Balanced citric acid (freshness)
✅ Controlled sulphates

Lower quality wines tend to have:
❌ High volatile acidity (vinegar taste)
❌ Low alcohol content
❌ Poor fermentation control
```

---

## 🛠️ Analysis Pipeline

```
WineQT Dataset (1,143 red wine samples)
        ↓
Exploratory Data Analysis
(distributions, correlation heatmap)
        ↓
Z-Score Standardization
(all 11 features scaled equally)
        ↓
Principal Component Analysis (PCA)
(11 features → principal components)
        ↓
Kaiser's Criterion (eigenvalue > 1)
(retain 7 components, drop 4)
        ↓
Scree Plot Visualization
(confirm elbow at PC7)
        ↓
Component Interpretation
(map each PC to winemaking concept)
        ↓
Business Recommendations
```

---

## 💡 Business Recommendations

**1. 🍶 Optimize alcohol levels**
Target 11–13% alcohol — the single variable with the strongest positive quality correlation (+0.48). Small increases in alcohol content yield measurable quality improvements.

**2. 🧫 Control volatile acidity**
Strengthen fermentation monitoring to minimize volatile acidity — the biggest quality detractor (−0.39). Even small reductions have outsized quality impact.

**3. 📊 Use PC profiles as a QA dashboard**
Track PC1 (Acidity), PC2 (Alcohol/Quality) and PC3 (Sulfur Dioxide) as real-time production indicators. These three components alone capture the most quality-relevant variation.

**4. 🤖 Build a predictive model next**
Use the 7 PCs as inputs to a regression or classification model to predict quality scores before bottling — enabling proactive intervention rather than reactive quality control.

---

## ⚠️ Limitations
- Red wine only — findings may not generalize to white or rosé varieties
- Quality scores are human-assigned and subjective — may vary across tasting panels
- Correlation ≠ Causation — PCA reveals co-variation patterns, not causal relationships
- Experimental validation needed to confirm that changing a variable directly improves ratings

---

## 🔧 Tools & Libraries
- Python
- Pandas / NumPy
- Scikit-learn (PCA, StandardScaler)
- Matplotlib / Seaborn
- WineQT Dataset (Kaggle)

---

## 📁 Files
| File | Description |
|------|-------------|
| `M3_Project_WineQuality_Poster_FINAL.pdf` | Full research poster with all findings and visualizations |

---

## 🔗 Related Projects
👉 [Credit Default Risk Prediction — Logistic Regression](https://github.com/Tariro-Kureva/Credit-Default-Risk-Prediction)
👉 [Seattle Crime Pattern Analysis — XGBoost & Logistic Regression](https://github.com/Tariro-Kureva/Seattle-Crime-Pattern-Analysis)
👉 [IBM HR Analytics — K-Means Clustering & Attrition](https://github.com/Tariro-Kureva/IBM-HR-Analytics-Clustering)
👉 [IMDB Sentiment Analysis — NLP & Machine Learning](https://github.com/Tariro-Kureva/IMDB-Sentiment-Analysis-NLP)
👉 [MovieLens Rating Analysis — Collaborative Filtering](https://github.com/Tariro-Kureva/MovieLens-Rating-Analysis)
👉 [Movie Plot Narrative Similarity — SentenceTransformers](https://github.com/Tariro-Kureva/Movie-Plot-Narrative-Similarity)
👉 [Extreme Disaster Events in Southern Africa — Power BI](https://github.com/Tariro-Kureva/Extreme-disaster-events-Southern-Africa)

---

*Last updated: April 2026*

