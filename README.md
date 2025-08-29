# Toronto Crime Analytics & Prediction

Analyze and forecast Toronto crime using Python. This repo contains two Jupyter notebooks: one for exploratory data analysis (EDA) with geospatial mapping and one for training/benchmarking predictive models.

## 🔎 Overview
- Explore **Assault** and **Auto Theft** patterns by area and time.
- Build and compare ML models (Gradient Boosting, Random Forest, Linear/XGBoost).
- Evaluate with **MSE, MAE, RMSE, R²** and export clean result tables.
- Produce interactive **Folium** maps (GeoPandas) for spatial insight.

## 📁 Notebooks
1. **Gson Data Analytics Toronto Crime Statistics.ipynb**
   - Cleans and joins geospatial data (GeoPandas), renders **Folium** maps.
   - Trains an **XGBoost Regressor** (e.g., predicting assault counts).
   - Outputs metrics and an “Actual vs Predicted” comparison table.

2. **Toronto Crime Statiscal Prediction.ipynb**
   - Ingests **Assault** and **Auto Theft** datasets.
   - Trains/compares **GradientBoostingRegressor**, **RandomForestRegressor**, **LinearRegression** with **train/test split**, **cross-validation**, and **GridSearchCV**.
   - Exports performance summaries and error tables; saves plots to `/mnt/data/plots`.

## 🧰 Tech Stack
- **Data/ML:** pandas, numpy, scikit-learn, xgboost
- **Geo/Maps:** geopandas, folium
- **Viz:** matplotlib, seaborn
- *(Some notebooks also import panel, pyngrok, gradio, jupyter_bokeh.)*

## 📦 Data
- Expected CSVs (example): `Assault.csv`, `AutoTheft.csv`
- Place in a local `data/` folder (or update paths inside the notebooks).
- If using Colab, replace upload cells with direct `pd.read_csv("data/<file>.csv")` or use the built-in upload prompt.

## ▶️ How to Run
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
# (optional) python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
