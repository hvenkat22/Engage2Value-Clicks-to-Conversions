# 📊 Google Web Analytics: Engage2Value

A data-driven predictive modeling project aimed at uncovering the key drivers of customer purchases from clickstream data on a digital commerce platform. The pipeline predicts session-level **purchase value** using advanced machine learning models and presents business-ready insights through an interactive Power BI dashboard.

---

## 🚀 Project Overview

- **Objective:** Predict the `purchaseValue` (total monetary value spent) for each user session based on session metadata, behavioral signals, traffic source, and device characteristics.
- **Dataset:** 100k+ sessions from a large-scale e-commerce platform, capturing user behavior, acquisition channels, device info, and geographic data.
- **Impact:** Helps digital marketing and product teams understand what drives conversion and optimize strategies accordingly.

---

## 🔧 Tech Stack

| Component       | Tools Used                                  |
|----------------|----------------------------------------------|
| Programming     | `Python`                                    |
| Data Wrangling  | `Pandas`, `NumPy`                           |
| Modeling        | `Scikit-learn`, `XGBoost`, `Random Forest`  |
| Visualization   | `Power BI`                                  |
| Evaluation      | R² Score (~0.72)                            |

---

## 🧠 Methodology

### 1. Data Exploration & Preprocessing
- Analyzed 50+ features across behavioral, device, traffic, and geo dimensions.
- Handled missing values, encoded categorical variables, and normalized continuous features.
- Created meaningful features such as session length, bounce rate indicators, and channel groupings.

### 2. Feature Engineering
- Derived time-based features from `sessionStart` (hour, day of week).
- Mapped device/browser strings to major categories.
- Grouped sparse categories (e.g., rare cities or referral paths) to reduce noise.

### 3. Modeling
- Trained ensemble regression models: **Random Forest** and **XGBoost**.
- Hyperparameter tuning using grid search and cross-validation.
- Achieved **R² score of ~0.72**, indicating strong model performance in predicting purchase value.

### 4. Insights & Visualization
- Designed a **Power BI Dashboard** to visualize:
  - Key drivers of purchase behavior.
  - Conversion trends by geography, device, and traffic source.
  - Session-level engagement metrics.

---

## 🧾 Feature Categories

### 📈 User Behavior & Session Metrics
- `totalHits`, `pageViews`, `totals.bounces`, `totals.visits`, `sessionNumber`, `sessionStart`

### 💻 Device & Technical Attributes
- `deviceType`, `os`, `browser`, `screenSize`, `device.language`, `gclIdPresent`

### 📣 Traffic & Marketing Source
- `userChannel`, `trafficSource.medium`, `trafficSource.keyword`, `adwordsClickInfo.*`, `referralPath`, `isTrueDirect`

### 🌍 Geographical Context
- `geoNetwork.city`, `locationCountry`, `geoNetwork.continent`, `geoCluster`, `locationZone`

### 🔑 Identifiers
- `userId`, `sessionId` (used for session tracking; not included in the model)

### 🎯 Target Variable
- `purchaseValue`: Amount spent during a session (regression target).


---

---

## 📁 Folder Structure

