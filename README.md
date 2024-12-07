# Exploring Transportation Access and Poverty in Michigan Census Tracts

This repository contains materials and code supporting a project investigating the relationship between transportation access (walkability, cyclability, and public transportation availability) and economic outcomes (specifically poverty) in Michigan census tracts. The project focuses on areas with low walkability, cyclability, and limited public transit options, often characterized by a high dependency on cars. The analysis aims to determine whether these mobility-constrained areas are associated with higher poverty rates.

**Institutional Context:**  
This work is intended for use at Michigan State University as part of CSE 881 (Data Mining), demonstrating practical applications of advanced data mining and machine learning methods to socio-economic and geospatial datasets.

## Overview

### Key Files
- **Final Code Notebook:**  
  `881_Project_Models_Dec4_2_Final.ipynb`  
  This Jupyter Notebook contains the final and most recent code used for data preprocessing, feature engineering, model training, and evaluation. Both explainable AI methods (Linear Regression, Logistic Regression) and "black-box" models (KNN, Random Forest, XGBoost, and a Graph Neural Network) are included.

- **Full-Size Dataset:**  
  `881_full_data_2024-11-14_181745.csv`  
  This dataset consolidates ACS (American Community Survey) demographic and economic data alongside WalkScore metrics. It contains the features and labels used throughout the analysis.

### Data Sources
1. **American Community Survey (ACS)**  
   The ACS is a survey administered by the U.S. Census Bureau, providing detailed demographic, economic, housing, and transportation information at various geographic levels.  
   - **Website:** [https://www.census.gov/programs-surveys/acs](https://www.census.gov/programs-surveys/acs)

2. **WalkScore**  
   WalkScore provides detailed walkability, bikeability, and transit accessibility metrics for geographic locations. The proprietary scoring system helps quantify how easily people can access daily services on foot, by bicycle, or via public transit.  
   - **Website:** [https://www.walkscore.com](https://www.walkscore.com)

### Methods
- **Explainable Models:** Linear Regression, Logistic Regression  
- **Black-Box Models:** KNN, Random Forest, XGBoost, Graph Neural Networks (GNN)

These models were chosen to compare easily interpretable approaches to more sophisticated, less interpretable methods. GNNs were incorporated to capture geospatial relationships between census tracts, potentially unveiling patterns not visible to traditional machine learning models.

### Hypothesis
The central hypothesis is that lower accessibility scores—represented by walk, bike, and transit scores—are associated with higher poverty rates. The binary classification threshold is set at a 20% poverty rate to delineate impoverished vs. not impoverished communities.

### Results
Initial results from linear regression and logistic regression suggest a complex relationship. Contrary to our initial hypothesis, higher walkability and cyclability often correlated with higher poverty rates in the linear model. Classification models (KNN, Random Forest, XGBoost, GNN) vary in performance, and the GNN provides unique insights by leveraging the graph structure of the data.

### Future Work
- Incorporate additional geospatial features and refine the graph construction methods for the GNN.  
- Explore advanced XAI techniques (e.g., LIME, SHAP) to interpret the more complex models.  
- Implement more robust cross-validation and hyperparameter tuning to improve model generalizability and performance consistency.

## Usage
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/your-repo.git
