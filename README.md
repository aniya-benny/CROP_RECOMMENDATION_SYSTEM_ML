# Crop Recommendation System — Machine Learning

An end-to-end Machine Learning project that recommends the most suitable crop to grow based on soil conditions, environmental factors, and water availability. Built using Python and Scikit-learn, with an interactive web interface powered by Gradio.

---

## Project Overview

Farmers often struggle to decide which crop to grow based on their land and climate conditions. Wrong crop choices lead to poor yield and financial loss. This system solves that problem by taking 11 soil and environmental parameters as input and predicting the most suitable crop using a trained Machine Learning model.

---

## Key Highlights

| Detail | Value |
|---|---|
| Language | Python |
| IDE | Jupyter Notebook |
| ML Library | Scikit-learn |
| UI Framework | Gradio |
| Models Compared | 7 |
| Best Model | Random Forest |
| Deployment | Pickle + Gradio Web UI |

---

## Features

- Full Exploratory Data Analysis (EDA) with visualisations
- Label Encoding for categorical features
- 7 ML models trained, evaluated and compared
- Interactive web UI built with Gradio — no coding needed to use
- Model and encoders saved using Pickle for reuse

---

## Models Trained and Compared

| Model | Evaluation Metrics Used |
|---|---|
| Logistic Regression | Accuracy, Precision, Recall, Confusion Matrix |
| Decision Tree | Accuracy, Precision, Recall, Confusion Matrix |
| Random Forest | Accuracy, Precision, Recall, Confusion Matrix |
| K-Nearest Neighbours (KNN) | Accuracy, Precision, Recall, Confusion Matrix |
| Support Vector Machine (SVM) | Accuracy, Precision, Recall, Confusion Matrix |
| Naive Bayes | Accuracy, Precision, Recall, Confusion Matrix |
| Gradient Boosting | Accuracy, Precision, Recall, Confusion Matrix |

**Random Forest was selected as the final model** due to its highest accuracy across all evaluation metrics.

---

## Visualisations

The notebook includes the following EDA charts:

- **Crop Distribution** — horizontal bar chart showing count of each crop in the dataset
- **Correlation Heatmap** — shows relationships between all numerical features
- **Boxplot for Outlier Detection** — identifies outliers across all feature columns
- **Soil Type vs Crops** — count plot showing which crops grow in which soil types
- **Season vs Crops** — count plot showing crop distribution across seasons

---

## Input Features

The model takes the following 11 parameters as input:

| Feature | Description |
|---|---|
| Soil Type | Type of soil (categorical) |
| Season | Growing season (categorical) |
| Water Source | Source of irrigation (categorical) |
| Soil pH | pH level of the soil |
| Crop Duration | Duration of the crop cycle |
| Temperature | Average temperature (°C) |
| Water Required | Water requirement of the crop |
| Relative Humidity | Humidity percentage |
| Nitrogen (N) | Nitrogen content in soil |
| Phosphorus (P) | Phosphorus content in soil |
| Potassium (K) | Potassium content in soil |

---

## Dataset

The dataset used is **Crop Recommendation Dataset** (`Crop recommendation dataset (1).csv`), containing records of various crops with their corresponding soil and environmental conditions.

Columns dropped during preprocessing (not relevant to prediction):
`TYPE_OF_CROP`, `SOWN`, `HARVESTED`, `SOIL_PH_HIGH`, `CROPDURATION_MAX`, `MAX_TEMP`, `WATERREQUIRED_MAX`, `RELATIVE_HUMIDITY_MAX`, `N_MAX`, `P_MAX`, `K_MAX`

---

## Tech Stack

| Tool / Library | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data loading and preprocessing |
| NumPy | Numerical operations |
| Matplotlib | Data visualisation |
| Seaborn | Statistical visualisation |
| Scikit-learn | ML model training and evaluation |
| Gradio | Interactive web UI |
| Pickle | Model and encoder serialisation |

---

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/aniya-benny/CROP_RECOMMENDATION_SYSTEM_ML.git
cd CROP_RECOMMENDATION_SYSTEM_ML
```

### 2. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn gradio
```

### 3. Open the notebook

```bash
jupyter notebook crop_rec_fixed.ipynb
```

### 4. Run all cells

Go to **Kernel → Restart & Run All**

This will:
- Load and preprocess the dataset
- Train all 7 models
- Evaluate and compare them
- Save the best model (`crop_model.sav`) and encoders (`.pkl` files) automatically
- Launch the Gradio web UI

### 5. Use the Gradio UI

After running all cells, a local URL will appear in the output (example: `http://127.0.0.1:7860`). Open it in your browser, fill in the soil and environmental values, and click **Submit** to get the recommended crop.

---

## Project Structure

```
CROP_RECOMMENDATION_SYSTEM_ML/
│
├── crop_rec_fixed.ipynb              # Main notebook with full ML pipeline
├── Crop recommendation dataset (1).csv  # Dataset
├── le_Soil.pkl                       # Label encoder for Soil column
├── le_Season.pkl                     # Label encoder for Season column
├── le_Water_Source.pkl               # Label encoder for Water Source column
└── README.md                         # Project documentation
```

> **Note:** The trained model file (`crop_model.sav`) is not included in this repository due to GitHub's 25 MB file size limit. It will be generated automatically when you run all cells in the notebook.

---

## Key Learnings

- How to perform EDA and feature selection on a real dataset
- Label encoding for categorical variables
- Training and comparing multiple ML classification models
- Evaluating models using Accuracy, Precision, Recall, and Confusion Matrix
- Building an interactive prediction UI using Gradio
- Saving and loading ML models using Pickle

---

## Author

**Aniya Benny**
Data Science Learner | Python | Machine Learning | Power BI | Tableau

Connect on [LinkedIn](#) | View more projects on [GitHub](https://github.com/aniya-benny)

---

## License

This project is open source and available under the [MIT License](LICENSE).
