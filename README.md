# 🧠 ArvyaX Emotional Intelligence System
### From Understanding Humans → To Guiding Them

---

## 🚀 Overview

This project builds an **end-to-end emotional intelligence system** that goes beyond prediction.

It is designed to:
- Understand human emotional states from noisy reflections
- Reason under imperfect and conflicting signals
- Decide meaningful next actions
- Guide users toward improved mental states

---

## 🧠 Approach

The system is structured into three layers:

### 1. Emotional Understanding
- Predicts:
  - `emotional_state` (classification)
  - `intensity` (regression: 1–5)
- Uses both:
  - Text (journal reflections)
  - Contextual signals (stress, energy, sleep, etc.)

---

### 2. Decision Layer (Core)
Transforms predictions into actionable guidance:

- **What to do**:
  - breathing, journaling, deep work, rest, etc.

- **When to do it**:
  - now, within_15_min, later_today, tonight

This layer combines:
- predicted state
- intensity
- stress
- energy
- time of day

---

### 3. Uncertainty Awareness
- Confidence score from model probabilities
- `uncertain_flag` for low-confidence predictions

This ensures the system **knows when it is unsure**

---

## ⚙️ Feature Engineering

### Text Features
- TF-IDF embeddings from `journal_text`
- Captures semantic patterns in reflections

### Metadata Features
- sleep_hours
- stress_level
- energy_level
- duration
- time_of_day

### Insight
> Text captures emotional meaning, while metadata provides behavioral context.

---

## 🤖 Model Choice

### Emotional State
- **LightGBM Classifier**
- Handles sparse + tabular data effectively
- Robust to noisy features

### Intensity Prediction
- **LightGBM Regressor**
- Models continuous emotional strength

### Why LightGBM?
- Fast and scalable
- Handles missing values well
- Strong performance on mixed feature types

---

## 🧭 Decision Engine

A rule-based but **context-aware system** that maps emotional understanding → action.

Example:
- High stress + low energy → breathing (now)
- Focused + high energy → deep work (now)
- Overwhelmed → journaling (soon)

---

## 📊 Dashboard

Built using **Plotly + ipywidgets (Colab UI)**

Features:
- Interactive filtering (state, action, uncertainty)
- Emotional distribution analysis
- Action recommendation patterns
- Confidence visualization

---

## ▶️ How to Run

1. Open the notebook in Google Colab
2. Install dependencies:
   # 🧠 ArvyaX Emotional Intelligence System
### From Understanding Humans → To Guiding Them

---

## 🚀 Overview

This project builds an **end-to-end emotional intelligence system** that goes beyond prediction.

It is designed to:
- Understand human emotional states from noisy reflections
- Reason under imperfect and conflicting signals
- Decide meaningful next actions
- Guide users toward improved mental states

---

## 🧠 Approach

The system is structured into three layers:

### 1. Emotional Understanding
- Predicts:
  - `emotional_state` (classification)
  - `intensity` (regression: 1–5)
- Uses both:
  - Text (journal reflections)
  - Contextual signals (stress, energy, sleep, etc.)

---

### 2. Decision Layer (Core)
Transforms predictions into actionable guidance:

- **What to do**:
  - breathing, journaling, deep work, rest, etc.

- **When to do it**:
  - now, within_15_min, later_today, tonight

This layer combines:
- predicted state
- intensity
- stress
- energy
- time of day

---

### 3. Uncertainty Awareness
- Confidence score from model probabilities
- `uncertain_flag` for low-confidence predictions

This ensures the system **knows when it is unsure**

---

## ⚙️ Feature Engineering

### Text Features
- TF-IDF embeddings from `journal_text`
- Captures semantic patterns in reflections

### Metadata Features
- sleep_hours
- stress_level
- energy_level
- duration
- time_of_day

### Insight
> Text captures emotional meaning, while metadata provides behavioral context.

---

## 🤖 Model Choice

### Emotional State
- **LightGBM Classifier**
- Handles sparse + tabular data effectively
- Robust to noisy features

### Intensity Prediction
- **LightGBM Regressor**
- Models continuous emotional strength

### Why LightGBM?
- Fast and scalable
- Handles missing values well
- Strong performance on mixed feature types

---

## 🧭 Decision Engine

A rule-based but **context-aware system** that maps emotional understanding → action.

Example:
- High stress + low energy → breathing (now)
- Focused + high energy → deep work (now)
- Overwhelmed → journaling (soon)

---

## 📊 Dashboard

Built using **Plotly + ipywidgets (Colab UI)**

Features:
- Interactive filtering (state, action, uncertainty)
- Emotional distribution analysis
- Action recommendation patterns
- Confidence visualization

---

## ▶️ How to Run

1. Open the notebook in Google Colab
2. Install dependencies:
   pip install lightgbm shap plotly seaborn
3. Upload:
- `train.csv`
- `test.csv`
4. Run all cells sequentially
5. Output:
- `predictions.csv`
- Interactive dashboard

---

## 📦 Output

### predictions.csv

Contains:
- id
- predicted_state
- predicted_intensity
- confidence
- uncertain_flag
- what_to_do
- when_to_do

---

## 🚀 Future Improvements

- Replace TF-IDF with BERT embeddings
- Learn decision policies (RL-based)
- Deploy as real-time mobile assistant

---

## ✨ Key Takeaway

This system demonstrates how AI can move from:
> **Prediction → to meaningful human guidance**
