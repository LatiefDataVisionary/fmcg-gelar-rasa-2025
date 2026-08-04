# FMCG Sales Predictive Analysis & Trend Forecasting - Gelar Rasa 2025

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)
<a href="https://colab.research.google.com/github/LatiefDataVisionary/fmcg-gelar-rasa-2025/blob/main/notebooks/notebook.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

---

## 👥 Data Analysis Team

*   **Team Name**: Trio Ireng
*   **University**: Universitas Teknologi Yogyakarta
*   **Team Members**:
    1.  Lathif Ramadhan
    2.  Rafi Ramadhan
    3.  Gilbert Mathew

---

## 🚀 Project Description & Objectives

This repository contains the data analysis and predictive modeling development for the **Data Science Competition "Gelar Rasa 2025"** organized by the Data Science Student Association (HIMASADA) at UPN "Veteran" East Java. 

Guided by the competition theme, ***"Revealing Hidden Patterns for Innovation and Strategic Growth in the Digital Era,"*** this project aims to dive deep into a synthetic transactional dataset of FMCG products within the *Personal Care* category. By leveraging historical and predictive data from 2020 to 2025, the project focuses on transforming raw data into strategic business insights that can drive sustainable growth in a highly competitive digital landscape.

The primary analytical objectives of this project are divided into three main pillars:

1.  **💡 Innovation Radar**: Analyzing individual and aggregate product performance to identify "rising stars" in the market. This involves highlighting products with the highest sales growth potential, identifying the most preferred product attributes (such as brand, type, or size), and understanding the correlation between marketing campaigns and a product's market traction.
2.  **📈 Trend Forecasting**: Developing robust machine learning models to forecast future sales trends and revenue. The focus is on understanding shifts in consumer preferences across various sales channels and regions, providing a fundamental basis for companies in planning inventory, marketing, and resource allocation strategies.
3.  **🔄 Product Cannibalization Analysis**: Conducting quantitative case studies to evaluate whether new product launches negatively impact (*cannibalize*) the sales of existing products within the same portfolio. This analysis provides data-driven recommendations regarding product launch strategies to maximize overall category growth.

---

## 📋 Table of Contents

- [Repository Structure](#-repository-structure)
- [Installation & Setup](#-installation--setup)
- [Dataset Description](#-dataset-description)
- [Project Workflow](#-project-workflow)
- [Results & Findings Summary](#-results--findings-summary)
- [Requirements](#-requirements)
- [Contributors](#-contributors)
- [License](#-license)

---

## 📂 Repository Structure

This project is organized with a systematic folder structure to ensure readability, scalability, and reproducibility.

```text
├── data/              # Folder for datasets (not tracked by Git due to size)
│   ├── raw/           # Raw data provided by the competition
│   └── processed/     # Cleaned and processed data ready for modeling
├── notebooks/         # Contains Jupyter Notebooks for analysis & experiments
├── reports/           # Final analysis results, visualizations, and reports
│   └── figures/       # Generated charts and plots
├── src/               # Modular source code (functions & pipelines)
├── submissions/       # Final notebook for competition submission
├── .gitignore         # Specifies intentionally untracked files to ignore
├── README.md          # This document
└── requirements.txt   # List of Python dependencies required to run the project
```

---

## ⚙️ Installation & Setup

To run this analysis in your local environment, please follow these steps:

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/LatiefDataVisionary/fmcg-gelar-rasa-2025.git
    cd fmcg-gelar-rasa-2025
    ```

2.  **Create a Virtual Environment** (Recommended)
    ```bash
    python -m venv venv
    source venv/bin/activate  # For Windows: venv\Scripts\activate
    ```

3.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Dataset Configuration**
    -   Download the competition dataset from the provided link: `bit.ly/DatasetDSCGelarRasa2025`.
    -   Extract the zip file and place all `.csv` files (`products.csv`, `marketing.csv`, `reviews.csv`, `sales.csv`) into the `data/raw/` directory.
    -   *Important Note*: These data files are intentionally not tracked by Git due to their large file size.

---

## 📊 Dataset Description

The analysis is based on the **"FMCG Personal Care - Synthetic Dataset"**, which simulates real transaction patterns in the Fast-Moving Consumer Goods (FMCG) industry for the personal care category, covering the period from **January 1, 2020, to December 31, 2025**. 

The dataset consists of four main interconnected files:

*   **`sales.csv`**: The core transactional dataset containing **~1,000,000 rows**. Key columns include `transaction_id`, `date`, `product_id`, `region`, `channel`, `units_sold`, `avg_price`, `discount_pct`, and `revenue`.
*   **`products.csv`**: Master data for 15 unique products. Key columns include `product_id`, `product_name`, `brand`, `type`, `size_ml`, `base_price`, and `launch_date`.
*   **`marketing.csv`**: Data on marketing campaigns. Key columns include `campaign_id`, `product_id`, `spend`, `channel`, and `engagement_rate`.
*   **`reviews.csv`**: A sample of **~10,000 customer reviews**. Key columns include `product_id`, `rating`, `sentiment`, and `comment`.

Further details regarding each column can be found in the `README_FMCG_Personal_Care.txt` file and within the Exploratory Data Analysis (EDA) section of the project.

---

## 🔬 Project Workflow

This project follows a highly structured and professional data science workflow:

1.  **Setup & Initialization**: Preparing the environment, importing essential libraries (Pandas, NumPy, Scikit-Learn, XGBoost, LightGBM), and loading the datasets.
2.  **Exploratory Data Analysis (EDA)**: Conducting descriptive statistics, univariate/bivariate/multivariate analysis, and data quality checks to understand data characteristics and uncover initial insights.
3.  **Data Preprocessing & Outlier Handling**: Cleaning the data by handling missing values, duplicates, and anomalies. Implementing statistical methods like Winsorization to handle extreme outliers in revenue and units sold, and managing pre-launch data anomalies.
4.  **Feature Engineering**: Creating highly creative and impactful new features to enrich the dataset. This includes time-based features (seasonality, weekends), Lag features (historical momentum), Rolling window averages, and Lifecycle indicators (e.g., `is_pre_launch`, `is_new_product_era`).
5.  **Modeling & Evaluation**: Building and comparing predictive pipelines using state-of-the-art Machine Learning algorithms (Linear Regression, Random Forest, XGBoost, and LightGBM). Training the models on historical data and evaluating their performance on validation sets using industry-standard metrics (MSE, RMSE, MAPE).
6.  **Product Cannibalization Study**: Conducting quantitative and visual case studies to evaluate the interactions between newly launched products and existing internal competitors.
7.  **Innovation Analysis & Presentation**: Synthesizing all analyses, models, and findings into a cohesive narrative. Presenting the results through clear, interactive dashboard-style visualizations and providing strategic, data-driven business recommendations.

---

## 📈 Results & Findings Summary

Based on the comprehensive analysis and modeling conducted in this project, we have successfully extracted several key strategic insights:

### **1. Trend Forecasting Excellence**
*   **Superior Model Performance**: Tree-based Gradient Boosting models significantly outperformed traditional linear baselines and standard Random Forests. **LightGBM** emerged as the champion model, achieving an impressive **R² score of approximately 0.60** and a **MAPE of ~13.8%** for daily revenue forecasting.
*   **Primary Sales Drivers**: Feature importance analysis revealed that future sales are heavily influenced by temporal patterns (seasonality, month, week of the year) and historical momentum (Lag features of revenue and units sold). Furthermore, intrinsic product characteristics (brand, type) and complex interactions between pricing and weekend discounts play a crucial role in driving revenue.

### **2. Innovation Radar & Rising Stars**
*   **Lifecycle Dynamics & Pre-launch Potential**: The engineered feature `is_pre_launch` successfully captured significant market anticipation. The model identified products that generated massive traction and sales even before their official release date, proving the effectiveness of teaser campaigns and pre-order strategies.
*   **Top Consumer Preferences**: Consumer demand is heavily skewed towards larger packaging sizes, specifically **340ml and 400ml**, which consistently drive the highest revenue. The **Shampoo** category remains the dominant volume driver in the portfolio.
*   **Identifying Growth**: Products from **Ponds** and **Sunsilk** variants demonstrated the strongest Year-over-Year growth momentum, marking them clearly as the portfolio's "Rising Stars" during their initial launch eras.

### **3. Strategic Cannibalization Insights**
*   **Parallel Growth, No Cannibalization**: In-depth case studies (e.g., analyzing the launch of PC014 against the existing PC003, and PC001 against PC013) revealed **no significant cannibalization**. 
*   **Market Expansion**: Instead of eroding existing market share, older products actually experienced a slight sales increase (up to **+9.16%**) following the new launches. This indicates a healthy overall category growth and suggests that the new products successfully reached untapped segments or fulfilled different consumer needs, effectively expanding the total market size.

---

## 🛠️ Requirements

To ensure full reproducibility of this analysis, the following Python libraries are required:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `xgboost`
- `lightgbm`
- `statsmodels`

*(A complete list with specific versions can be found in the `requirements.txt` file).*

---

## 👥 Contributors

*   **Lathif Ramadhan** 
*   **Rafi Ramadhan** 
*   **Gilbert Mathew** 

---

## 📜 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
