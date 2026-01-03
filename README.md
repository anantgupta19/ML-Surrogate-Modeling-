# ML Surrogate Modeling of Radiant Heat Flux (NIST Fire Data)

This repository presents a machine learning–based surrogate modeling approach for predicting **radiant heat flux** using experimental fire data from the **NIST Composite Floor Test (No. 1)**.

The core idea of this work is to learn CFD-derived fire quantities using data-driven models, with the long-term motivation of accelerating **CFD–FEM fire–structure interaction workflows** by replacing repeated high-cost simulations with fast ML surrogates.

---

## 🔍 Project Motivation

Fire-driven simulations such as CFD (for fire dynamics) and FEM (for structural response) are computationally expensive, especially for transient and parametric studies.  
This project explores whether ML models can learn the relationship between key fire parameters (e.g., HRR, gas composition, mass flow) and **radiant heat flux**, which is a critical thermal boundary condition for structural analysis.

---

## 📊 Dataset

- **Source:** NIST – CompositeFloorTest_No1  
- **Type:** Experimental fire test data  
- **Inputs include:**
  - Time
  - Heat Release Rate (HRR)
  - Burner HRR
  - Exhaust mass flow rate
  - Oxygen, CO₂, CO volume fractions
  - Smoke extinction coefficient (Ksmoke)
- **Target variable:**
  - Radiant Heat Flux (kW/m²)

---

## 🧠 Methodology

The workflow follows a progressive modeling strategy:

1. **Data inspection and minimal cleaning**
2. **Baseline ML model (Linear Regression)**  
   - Physics-aware sanity check
3. **Nonlinear surrogate modeling**
   - Captures complex fire dynamics
4. **Evaluation using MAE and R²**
5. **Conceptual integration**
   - ML surrogate positioned as a replacement for CFD loops
   - Output can serve as input to FEM-based structural models

The emphasis is on **interpretability, robustness, and engineering relevance**, rather than overfitting or excessive model complexity.

---

## 🚀 Potential Extensions

- Time-aware surrogate modeling (transient fire behavior)
- Coupling with FEM-based structural response models
- Physics-informed ML constraints
- Deployment as a lightweight decision-support or teaching tool

---

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- (Optional extensions: XGBoost, Streamlit)

---

## 📌 Disclaimer

This work focuses on surrogate modeling of **fire-side quantities only**.  
Structural response prediction requires coupling with FEM models and material behavior, which is beyond the scope of this repository.

---

## 👤 Author

**Anant Dev Gupta**  
Student | Fire Engineering & ML Enthusiast  

---

## 📬 Feedback

Suggestions, critiques, and discussions are welcome.
