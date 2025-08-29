# Toronto Crime Analytics & Prediction

This repository contains two Jupyter notebooks that analyze and forecast crime statistics in Toronto. The project combines exploratory data analysis (EDA), geospatial mapping, and predictive modeling to uncover crime patterns and build machine learning models that evaluate and forecast incidents such as Assaults and Auto Thefts. The goal is to provide insights that can support policy, law enforcement strategies, and academic research.

The first notebook, **Gson Data Analytics Toronto Crime Statistics.ipynb**, focuses on exploratory analysis and mapping. It loads Assault data, processes it with pandas and GeoPandas, and creates an interactive map using Folium to visualize crime distribution across the city. It also applies an XGBoost regressor to predict assault cases by area, evaluates model performance using Mean Squared Error (MSE) and R², and generates an “Actual vs Predicted” comparison table.

The second notebook, **Toronto Crime Statiscal Prediction.ipynb**, builds and compares multiple machine learning models including Gradient Boosting, Random Forest, and Linear Regression. It works with both Assault and Auto Theft datasets, splitting data into training and test sets, applying cross-validation, and running GridSearchCV for hyperparameter tuning. The notebook exports clean CSV summaries such as cross-validation results, model performance scores, and error/accuracy tables for both datasets. It also saves model comparison plots and error visualizations into a dedicated folder for easier analysis.

## Objectives
- Conduct exploratory data analysis to identify patterns in Toronto crime statistics.  
- Apply geospatial mapping techniques to visualize crime locations and densities.  
- Build and evaluate predictive models for crime forecasting using tree-based and linear methods.  
- Export reproducible results, error reports, and visualizations for decision-making.  

## Tools and Technologies
- **Languages and Libraries:** Python, Pandas, NumPy, Scikit-learn, XGBoost  
- **Geospatial and Mapping:** GeoPandas, Folium  
- **Visualization:** Matplotlib, Seaborn  
- **Other Utilities:** Panel, Pyngrok, Gradio, Jupyter Bokeh (imported in some workflows)  

## Data
The notebooks expect CSV input files such as `Assault.csv` and `AutoTheft.csv`. In local runs, these files should be placed in a `data/` folder or paths updated accordingly. In Colab, the prediction notebook allows uploading via the Google Colab file upload widget. If running locally, replace that with a direct `pd.read_csv("data/filename.csv")`.

## Outputs
Running the notebooks generates several useful outputs:
- CSV files including `Cross_Validation_Results.csv`, `Model_Performance_Summary.csv`, `Assault_Actual_vs_Predicted_Errors_Accuracy.csv`, and `AutoTheft_Actual_vs_Predicted_Errors_Accuracy.csv`.  
- Plots saved in `/mnt/data/plots` illustrating model comparisons, actual vs predicted values, and error distributions.  
- Interactive Folium map for spatial analysis of Assault data.  

## Repository Structure
- `Gson Data Analytics Toronto Crime Statistics.ipynb` – Exploratory analysis, geospatial mapping, XGBoost model for Assaults.  
- `Toronto Crime Statiscal Prediction.ipynb` – Gradient Boosting, Random Forest, and Linear Regression applied to Assault and Auto Theft with cross-validation and exports.  
- `data/` – Optional directory for storing input CSV datasets.  
- `README.md` – Documentation of the project.  

## How to Run
1. Clone the repository and move into the project folder.  
2. Install dependencies such as pandas, numpy, scikit-learn, xgboost, geopandas, folium, matplotlib, and seaborn. You may also include panel, pyngrok, gradio, and jupyter-bokeh if needed.  
3. Place your data files (e.g., `Assault.csv`, `AutoTheft.csv`) in a `data/` folder or update file paths in the notebooks.  
4. Launch Jupyter Notebook and run either notebook step by step.  

## Roadmap
Future improvements may include time-series forecasting with Prophet, SARIMA, or LSTM models, publishing an interactive dashboard with Streamlit or Panel, and enriching geospatial maps with Toronto neighborhood or ward-level choropleths for deeper insights.  
