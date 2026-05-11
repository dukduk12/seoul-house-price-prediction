# 🏠 Seoul House Price Prediction  
### Upstage AI Lab 14th ML Competition | Team 3I1E

> 1st Place solution for large-scale Seoul apartment price prediction using ensemble learning, feature engineering, and geospatial analysis.

---

## 👥 Team

<div align="center">

| Team Leader | Data Scientist | Data Scientist | Data Scientist |
|:--:|:--:|:--:|:--:|
| <img src="https://github.com/dukduk12.png" width="120"/> | <img src="https://github.com/mingg210.png" width="120"/> | <img src="https://github.com/qpwpep.png" width="120"/> | <img src="https://github.com/BH-Min-lab.png" width="120"/> |
| [Heewon Ahn](https://github.com/dukduk12) | [Minji Jung](https://github.com/mingg210) | [Myeongcheol Kim](https://github.com/qpwpep) | [Byeongho Min](https://github.com/BH-Min-lab) |
| ML Pipeline / Feature Engineering / Ensemble | EDA / Validation | Modeling / Experimentation | Data Analysis / Research |

</div>

---

# 📌 Competition Overview

## Background

This project was conducted as part of the **Upstage AI Lab 14th Machine Learning Competition** focused on predicting Seoul apartment transaction prices using large-scale real estate transaction datasets.

The competition aimed to build highly generalizable regression models capable of handling complex non-linear relationships, regional locality, and temporal market trends.

---

## 🎯 Objectives

- Achieve competitive RMSE performance on hidden test sets
- Build an end-to-end machine learning workflow
- Improve model generalization through feature engineering and ensemble strategies
- Apply domain knowledge to real-world real estate data

---

# 📊 Dataset

| Dataset | Description |
|---|---|
| train.csv | ~1,118,822 apartment transaction records |
| test.csv | ~9,272 samples without target values |

### Main Features

- District (`시군구`)
- Floor
- Construction Year
- Contract Date
- Exclusive Area
- Address (`번지`)

### Target

- Apartment transaction price (`거래금액`)

---

# 🧠 Project Workflow

We adopted an iterative **CRISP-DM based workflow** with repeated experimentation cycles. :contentReference[oaicite:2]{index=2}

## 1️⃣ Data Analysis & Validation

- Missing value inspection
- Outlier detection
- Correlation analysis
- VIF analysis
- Distribution comparison between train/test sets
- Time-based error analysis

## 2️⃣ Feature Engineering

- Geospatial feature generation using Kakao API
- Latitude / Longitude extraction from address data
- Subway-distance features
- Regional pricing features
- COVID-period residual analysis
- External public dataset integration

## 3️⃣ Modeling

### Models Tested

- LightGBM
- Random Forest
- XGBoost
- CatBoost
- GRU
- MLP
- Neural Networks

### Strategies

- Ensemble Learning
- Stacking
- Soft Voting
- Surrogate Modeling
- Residual Correction
- Optuna Hyperparameter Tuning

---

# 📈 Key Insights

## 🔍 Generalization Matters More Than Public Score

During experimentation, we observed that aggressively engineered external features improved public RMSE but significantly harmed model generalization. :contentReference[oaicite:3]{index=3}

This led us to focus on:

- Reliable feature relationships
- Robust validation strategies
- Ensemble complementarity
- Temporal error analysis

---

## 📍 Location Was the Most Critical Feature

We discovered that apartment pricing was heavily influenced by precise location information.

To improve spatial understanding:

- Address data was converted into latitude/longitude
- District-level pricing statistics were generated
- Subway accessibility features were added

This significantly improved overall model performance. :contentReference[oaicite:4]{index=4}

---

# 🏆 Results

| Model | Public RMSE | Private RMSE |
|---|---|---|
| Ensemble (v3) | 17,989 | 11,747 |
| Surrogate (v8) | 14,489 | 13,091 |
| LightGBM (v8) | 16,194 | 11,534 |

---

## 🥇 Final Ranking

- **1st Place**
- Final RMSE: `13091.1472`

<p align="center">
  <img src="./Asset/outputs/leaderboard_capture.png" width="700"/>
</p>

---

# 🛠 Tech Stack

## Machine Learning

- Python
- Scikit-learn
- LightGBM
- XGBoost
- CatBoost
- PyTorch
- Optuna

## Data Analysis

- Pandas
- NumPy
- Matplotlib
- Seaborn

## Collaboration

- GitHub
- Notion
- Upstage GPU Server

---

# 🤝 Collaboration

Our team conducted daily scrum sessions throughout the competition period and continuously shared experimental results and validation findings. :contentReference[oaicite:5]{index=5}

We emphasized:

- Rapid experimentation
- Shared debugging
- Continuous validation
- Iterative feature refinement

---

# 📄 Presentation

👉 [Competition Presentation Slides](YOUR_LINK_HERE)

---

# 📚 Lessons Learned

- Feature engineering must prioritize generalization
- Spatial information is critical for real-estate ML tasks
- Ensemble models outperform isolated models in complex regression problems
- Consistent experimentation pipelines greatly improve team productivity

---

# 🌱 Future Work

- Graph Neural Networks (GNN)
- Geo-spatial regression
- Real-time external economic indicators
- Advanced temporal modeling
- Automated feature generation pipelines

