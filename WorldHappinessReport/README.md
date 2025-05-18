# 🌍 World Happiness Report Analysis

This notebook file contains a comprehensive **Exploratory Data Analysis (EDA)** and **Machine Learning modeling** of the **World Happiness Report dataset**, focusing on the 2015 data with integration across years from **2015 to 2019**.

The analysis explores how economic, social, and political factors such as GDP per capita, life expectancy, freedom, and trust influence happiness levels globally. Additionally, two machine learning models are trained to predict happiness scores based on these indicators.

---

## 📁 Project Structure


---

## 🔍 What’s Inside the Notebook?

### 1. **Data Loading & Inspection**
- The dataset (`WorldHappinessReport.csv`) is loaded using `pandas`.
- Initial inspection shows columns like:
  - `Country`, `Region`, `Happiness Rank`, `Happiness Score`
  - Economic, health, family, freedom, generosity, and trust metrics
- First few rows show top countries like Switzerland, Iceland, Denmark, etc.

### 2. **Data Cleaning**
- Checked for missing values — none found.
- Checked for duplicates — none found.
- Added a new column `Year = 2015` to later combine data across multiple years.

### 3. **Basic Statistics**
- Used `.describe()` to get statistical summaries.
- Showcased mean, standard deviation, min/max values for all numerical features.

### 4. **Data Visualization**
Various plots were generated to understand data distributions and relationships:

#### 📈 Histograms
- Distribution of happiness scores, GDP per capita, life expectancy, freedom, generosity, etc.

#### 🧮 Kernel Density Estimation (KDE) Plots
- Smoothed versions of histograms showing probability density functions.

#### 📊 Boxplots
- Showed distribution of happiness scores across different regions (e.g., Western Europe vs Sub-Saharan Africa).

#### 💬 Scatter Plots
- Economy (GDP per Capita) vs Happiness Score
- Health (Life Expectancy) vs Happiness Score

#### 🔗 Pairplots
- Automatically plotted pairwise relationships between all numerical variables.

---

## 🔄 Multi-Year Dataset Integration

To analyze trends over time:

- Loaded datasets for years 2016–2019.
- Standardized column names across years.
- Selected common features to keep consistency.
- Merged datasets into one combined DataFrame with an added `Year` column.
- Final combined dataset has **790 rows (158 countries × 5 years)** and 10 columns.

---

## 🔗 Correlation Analysis

Correlation matrices were computed for each year to see which factors most strongly influence happiness scores.

Key findings:
- Strong positive correlation between:
  - **Economy (GDP per Capita)** and Happiness Score
  - **Health (Life Expectancy)** and Happiness Score
- Moderate correlations with Family, Freedom, and Trust

Visualized using heatmaps with annotations.

---

## 🤖 Machine Learning Modeling (2019 Data)

Two regression models were trained to predict **Happiness Score** using the following input features:
- `Economy (GDP per Capita)`
- `Family`
- `Health (Life Expectancy)`
- `Freedom`
- `Generosity`
- `Trust (Government Corruption)`

### Models Trained:
1. **Linear Regression**
   - MSE: ~0.414
   - R² Score: ~0.602

2. **Random Forest Regressor**
   - MSE: ~0.386
   - R² Score: ~0.629

### Evaluation Metrics
- Mean Squared Error (MSE)
- R-squared (R²) score

### Visualization of Predictions
- Line plot comparing actual vs predicted happiness scores
- Scatter plots for both models showing how well predictions align with true values

---

## 🚀 How to Run the Notebook

### Requirements
Make sure you have the following installed:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
