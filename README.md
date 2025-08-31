# 🌊 River Flow Forecasting Using Machine Learning

This repository contains my MSc Dissertation project on **Daily River Flow Forecasting** conducted at **Cardiff University**.  
The study focuses on the **River Taff at Pontypridd (Station ID: 57005)** along with its **seven active tributaries**, using **gauged daily flow (GDF)** and **catchment daily rainfall (CDR)** data from the [National River Flow Archive (NRFA)](https://nrfa.ceh.ac.uk/data/search).

The project explores both **traditional statistical methods (Linear Regression)** and **advanced Machine Learning techniques (Support Vector Regression, Neural Networks, Generalised Additive Models)** with various data preprocessing methods to evaluate their forecasting accuracy.

---

## 📌 Objective
To develop predictive models for **next-day river flow forecasting** by combining rainfall and flow data across multiple gauges.  
The models aim to support **flood risk management, water resource planning, and disaster preparedness**.

---

## ⚡ Key Highlights
- 📊 **Data source**: [National River Flow Archive (NRFA)](https://nrfa.ceh.ac.uk/data/search) & Natural Resources Wales.  
- 🗓️ **Time period used**: 2006-05-26 → 2017-12-31.  
- 🔄 **Preprocessing techniques**:  
  - Log Transformation  
  - De-seasonalisation  
  - Box-Cox Transformation  
  - Feature Selection (Forward & Backward stepwise)  
- 🤖 **Models implemented**:  
  - Linear Regression (baseline)  
  - Support Vector Regression (SVR)  
  - Neural Network (NN)  
  - Generalised Additive Model (GAM)  
- 🎯 **Model optimisation**: Random Search CV for SVR (hyperparameter tuning + scaling).  
- 🏆 **Best performing model**: **SVR with Box-Cox transformed data**, achieving strong accuracy (MAPE ≈ 3.5%).  
- 🔮 **Next-day prediction**: The optimised SVR model produced reliable forecasts for the test period.

---

## 📂 Repository Contents
- `dataset/` → CSV files (GDF + CDR for each gauge).  
- `MSc_dissertation_2024_23039854_jones.ipynb` → Jupyter Notebook with all code (cleaning → EDA → preprocessing → model building → evaluation).  
- `problem_statement.pdf` → Original project problem statement.  
- `MSc_dissertation_2024_23039854_jones.pdf` → Dissertation report (public version, **declaration page removed for privacy**).  

---

## 🔄 Workflow

```mermaid
flowchart TD
    A[Data Acquisition] -->|NRFA Gauged Flow + Rainfall| B[Data Cleaning & Integration]
    B --> C[Exploratory Data Analysis]
    C --> D[Preprocessing]
    D --> D1[Log Transformation]
    D --> D2[De-seasonalisation]
    D --> D3[Box-Cox Transformation]
    D --> D4[Feature Selection (Forward + Backward)]

    D --> E[Model Building]
    E --> E1[Linear Regression (Baseline)]
    E --> E2[Support Vector Regression (SVR)]
    E --> E3[Neural Network]
    E --> E4[Generalised Additive Model]

    E2 --> F[Hyperparameter Optimisation (Random Search CV)]
    F --> G[Evaluation]

    E1 --> G
    E3 --> G
    E4 --> G

    G --> H[Model Comparison]
    H --> I[Best Model: SVR (Box-Cox Data)]
    I --> J[Next-Day Prediction]
```

---

## 📈 Results
- SVR consistently outperformed Linear Regression, Neural Network, and GAM.  
- Box-Cox transformed data improved variance stability and model accuracy.  
- Feature selection was found to influence predictive performance significantly.  
- Future work:  
  - Hyperparameter tuning of Neural Networks.  
  - Exploring ensemble methods (SVR + NN).  
  - Deeper investigation of feature selection techniques.

---

## 🙏 Acknowledgements
- **Supervisor**: Provided valuable guidance throughout the research.  
- **National River Flow Archive (NRFA)** & **Natural Resources Wales**: For providing gauged river flow and rainfall data.  

---

## 📬 Contact
👤 **Abhishek Kumar**  
📧 abhishekkumar.dsanalytics@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/) | [GitHub](https://github.com/)  

---
