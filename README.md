# 🎬 Movie Reviews Sentiment & Box Office Performance Analysis

##  Project Overview

This project combines natural language processing (NLP), machine learning, exploratory data analysis, revenue forecasting, and data visualization to explore movie review sentiment and box-office performance.

The project has two main analytical components: sentiment classification using IMDb movie reviews and box-office performance analysis using TMDB movie data. A Tableau dashboard presents key movie performance metrics and trends.

##  Objectives

- Analyze positive and negative movie reviews using NLP.
- Build and compare machine learning models for sentiment classification.
- Explore relationships among movie revenue, ratings, popularity, and release years.
- Evaluate forecasting models for yearly median movie revenue.
- Develop an interactive Tableau dashboard to communicate findings.

##  Tools and Technologies

- **Programming:** Python
- **Data Analysis:** pandas, NumPy
- **Machine Learning:** scikit-learn
- **Natural Language Processing:** TF-IDF, text preprocessing, sentiment classification
- **Data Visualization:** Matplotlib, Tableau
- **Forecasting:** Naive baseline, Damped Exponential Smoothing, Holt Linear Trend
- **Environment:** Jupyter Notebook

##  Datasets

### 1. IMDb Movie Reviews Dataset

Used for text preprocessing and sentiment classification.

- **Records:** 50,000 movie reviews
- **Features:** Review text and sentiment label
- **Target classes:** Positive and negative

### 2. TMDB 5000 Movies Dataset

Used for exploratory data analysis, box-office analysis, and forecasting.

- Movie titles, genres, and release dates
- Budget and revenue
- Popularity and average ratings
- Vote counts and movie overviews

The IMDb and TMDB datasets are analyzed separately because the IMDb review dataset does not contain movie identifiers that allow reliable matching of individual reviews to box-office revenue.

##  Methodology

### 1. Data Cleaning and Exploration

- Inspected dataset structure and missing values.
- Cleaned review text and removed HTML tags.
- Processed movie metadata and handled zero-valued budget and revenue entries as missing where appropriate.
- Explored movie ratings, revenue distributions, popularity, and release-year trends.

### 2. Sentiment Analysis

<img width="1780" height="970" alt="Sentiment Classification Model Comparison" src="https://github.com/user-attachments/assets/75af5c4d-f18f-41df-a38e-108deba0f90b" />

- Converted review text into numerical features using TF-IDF.
- Split the data into training and testing sets using an 80/20 split.
- Trained Logistic Regression and Multinomial Naive Bayes classifiers.
- Evaluated model performance using accuracy, precision, recall, F1-score, and confusion matrices.
- Tested the trained model on a new review.

### 3. Box-Office Performance Analysis

<img width="2246" height="1124" alt="Box Office Revenue Forecast" src="https://github.com/user-attachments/assets/d8713530-e675-44af-a575-2f6ac079f5fa" />

- Examined top-grossing movies.
- Analyzed ratings and popularity.
- Investigated yearly movie releases and revenue trends.
- Used vote-count filtering to reduce the influence of ratings based on very few votes.

### 4. Revenue Forecasting

 <img width="1252" height="950" alt="Logistic Regression Confusion Matrix" src="https://github.com/user-attachments/assets/04549349-97af-4c27-bc5a-5089adab84e2" />

Compared three forecasting approaches:

- Naive baseline
- Damped Exponential Smoothing
- Holt Linear Trend

Models were evaluated using a chronological train-test split and Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).

### 5. Tableau Dashboard
 
 <img width="3000" height="1976" alt="Tableau Dashboard" src="https://github.com/user-attachments/assets/92dc0768-88fd-4182-8e3f-9ec50889c3b5" />

Created a dashboard featuring:

- Total movie count
- Total recorded revenue
- Average movie rating
- Revenue by release year
- Top 10 movies by revenue
- Movie ratings versus box-office revenue

## Key Results

### Sentiment Classification

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Logistic Regression | **90.86%** | 90.34% | 91.50% | **90.92%** |
| Multinomial Naive Bayes | 87.96% | 87.42% | 88.68% | 88.05% |

Logistic Regression outperformed Multinomial Naive Bayes across all four evaluation metrics and was selected as the best-performing model among the two evaluated.

### Revenue Forecasting

The Naive baseline achieved the lowest test errors among the three evaluated models:

| Model | MAE | RMSE |
|---|---:|---:|
| Naive | $23.83 million | $28.86 million |
| Damped Exponential Smoothing | $28.46 million | $32.80 million |
| Holt Linear Trend | $28.66 million | $33.02 million |

The results indicate that the more complex trend-based models did not improve forecast accuracy over the Naive baseline for the selected test period.

*Note: Forecasting results are based on yearly median movie revenue and should be interpreted cautiously because the test period is relatively short.*

##  Skills Demonstrated

- Python programming
- Data cleaning and exploratory data analysis
- Natural Language Processing (NLP)
- Text mining and TF-IDF feature extraction
- Machine learning model development
- Classification model evaluation
- Time-series forecasting
- Data visualization and dashboard development
- Analytical storytelling

## How to Run the Project

1. Clone or download this repository.
2. Install the required Python packages.
3. Place the datasets in the appropriate data folder.
4. Open the notebooks in Jupyter Notebook or JupyterLab.
5. Run the notebook cells in order.
6. Open the Tableau workbook in Tableau Desktop to explore the dashboard.

Install the main dependencies with:

```bash
pip install pandas numpy scikit-learn matplotlib statsmodels jupyter
```

Update the dataset paths in the notebooks if your files are stored in a different location.

## Author

**Mahitha Kalinathabotla**

Data Analytics | Machine Learning | Natural Language Processing

Connect with me on [LinkedIn](www.linkedin.com/in/mahitha-kalinathabotla).
