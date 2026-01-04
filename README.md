# SpaceX Falcon 9 – EDA, SQL, Geospatial Analysis & Machine Learning
This project was developed as part of the *Applied Data Science Capstone* for the **IBM Data Science Professional Certificate**. It represents the culmination of the programme, integrating data acquisition, SQL analytics, exploratory data analysis, geospatial visualisation, and machine learning into a comprehensive, end‑to‑end data science workflow.
1. Project Overview:
   The objective of this project is to analyse SpaceX Falcon 9 launch data to understand the factors that influence landing success and to build predictive models capable of estimating the likelihood of a successful booster landing.
2. Project Structure:
   spacex-falcon9-analysis/
│
├── notebooks/
│   ├── 1 - jupyter_labs_spacex_data_collection_api_v2.ipynb
│   ├── 2 - jupyter-labs-webscraping.ipynb
│   ├── 3 - labs_jupyter_spacex_Data_wrangling.ipynb
│   ├── 4 - jupyter_labs_eda_sql_coursera_sqllite.ipynb
│   ├── 5- eda .ipynb
│   ├── 6 - lab_jupyter_launch_site_location (1).ipynb
│   └── 7 - machine learning  .ipynb
│
├── data/
│   ├── raw/
│   └── cleaned/
│
├── images/
│   ├── folium_map.png
│   ├── model_accuracy.png
│   └── additional_screenshots.png
│
├── src/
│   ├── utils.py
│   └── model_training.py
│
├── README.md
└── requirements.txt
3. SQL Analysis - Key Findings
   The SQL component of the project provided foundational insights, including:
- Identification of all unique launch sites
- Total payload mass delivered for specific customers (e.g., NASA CRS missions)
- Determination of the earliest successful ground landing
- Analysis of failed drone‑ship landings by year and month
- Identification of booster versions associated with the heaviest payloads
These queries established a strong analytical basis for subsequent EDA and modelling.

4. Exploratory Data Analysis (EDA)
The EDA phase revealed several important patterns:
- Launch success is influenced by orbit type, launch site, booster version, and payload mass
- Success rates have increased significantly over time, reflecting SpaceX’s engineering improvements
- Scatter plots, bar charts, and heatmaps highlighted relationships between mission characteristics and outcomes
- Categorical variables demonstrated clearer patterns than numerical correlations
These insights informed feature engineering and model selection.

5. Geospatial Visualisation (Folium Map)
An interactive Folium map was created to illustrate the geographical distribution of launch sites and mission outcomes.
Map Features:
- Marker clusters showing launch density
- Rocket icons coloured by mission outcome (success or failure)
- Pop‑up windows displaying mission details
- Fixed text labels identifying launch sites (e.g., LC‑40, LC‑39A, SLC‑4E)
Geospatial Insights:
- Florida (Cape Canaveral) hosts the majority of Falcon 9 launches
- California (Vandenberg) is primarily used for polar and sun‑synchronous missions
- Clustering patterns highlight operational specialisation across sites

6. Machine Learning Models
Several classification models were developed and evaluated:
- Logistic Regression
- K‑Nearest Neighbours (KNN)
- Decision Tree
- Support Vector Machine (SVM)
Model Performance:

| Model                            | Accuracy |
|----------------------------------|----------|
| Logistic Regression              | 0.85     |
| Decision Tree                    | 0.82     |
| K‑Nearest Neighbours             | 0.80     |
| **Support Vector Machine (SVM)** | **0.88** |

Best Performing Model: Support Vector Machine (SVM)
SVM achieved the highest accuracy due to:
- Effective handling of high‑dimensional feature spaces
- Ability to model non‑linear relationships
- Strong generalisation after hyperparameter tuning
This model provides the most reliable predictions for landing success.

7. Conclusions
- SpaceX’s landing success rate has improved markedly over the years
- Mission outcome is strongly influenced by orbit type, launch site, payload mass, and booster version
- Geospatial analysis revealed clear operational hubs and mission clustering
- The SVM model demonstrated superior predictive performance
- The project successfully integrates SQL, EDA, geospatial analysis, and machine learning into a cohesive analytical pipeline

8. How to Run the Project
1. Clone the repository:
git clone https://github.com/YOUR_USERNAME/spacex-falcon9-analysis.git
2. Install dependencies:
pip install -r requirements.txt
3. Open and run the notebooks:
Use Jupyter Notebook, JupyterLab, or VS Code to execute the files in the notebooks/ directory.

9. Requirements
The project uses the following key libraries:
- pandas
- numpy
- scikit‑learn
- folium
- matplotlib
- seaborn
- sqlite3 (or equivalent SQL connector)
All dependencies are listed in requirements.txt.

10. Author
Developed by Leilane as part of the Applied Data Science Capstone for the IBM Data Science Professional Certificate

