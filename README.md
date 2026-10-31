# Netflix Content Success Analytics Engine

## Project Overview

The Netflix Content Success Analytics Engine is a machine learning project designed to analyze Netflix content metadata, identify content patterns, and generate meaningful business insights.

The project uses data preprocessing, feature engineering, K-Means clustering, model evaluation, automated insights, and data visualization to understand different categories of Netflix Movies and TV Shows.

**Important:** The dataset contains content metadata but does not include actual views, watch time, audience engagement, or revenue. Therefore, this project identifies metadata-based content segments rather than predicting actual Netflix popularity or commercial success.

## Objectives

- Analyze Netflix Movies and TV Shows.
- Perform data cleaning and preprocessing.
- Apply advanced feature engineering.
- Identify content segments using machine learning.
- Compare clustering performance.
- Generate automated business insights.
- Create visual reports.
- Build reusable ML pipelines.

## Dataset Information

The dataset contains 8,790 records and 10 original columns.

**Columns:**
- show_id
- type
- title
- director
- country
- date_added
- release_year
- rating
- duration
- listed_in

Additional engineered features include:
- added_year
- added_month
- content_age
- genre_count
- country_count
- duration_value
- is_movie
- is_tv_show

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Joblib
- Google Colab

## Project Workflow

1. Data Collection and Loading
2. Data Cleaning and Preprocessing
3. Advanced Feature Engineering
4. Metadata-Based Content Scoring
5. Movie Content Segmentation using K-Means
6. TV Show Content Segmentation using K-Means
7. Clustering Performance Evaluation
8. Automated Business Insights
9. Data Visualization and Reporting
10. ML Pipeline Development and Model Saving

## Machine Learning Models

Separate K-Means clustering models were developed for Movies and TV Shows.

### Movie Clustering

- Total records: 6,126
- Number of clusters: 3
- Silhouette Score: 0.3476

**Identified segments:**

| Cluster | Movies | Segment |
|---|---:|---|
| 0 | 3,088 | Recent Long Movies |
| 1 | 2,486 | Recent Shorter Movies |
| 2 | 552 | Classic Movies |

### TV Show Clustering

- Total records: 2,664
- Number of clusters: 3
- Silhouette Score: 0.3944

**Identified segments:**

| Cluster | TV Shows | Segment |
|---|---:|---|
| 0 | 1,289 | Recent Multi-Genre Shows |
| 1 | 1,265 | Recent Focused-Genre Shows |
| 2 | 110 | Classic TV Shows |

## Model Evaluation

| Model | Clusters | Silhouette Score |
|---|---:|---:|
| Movie K-Means | 3 | 0.3476 |
| TV Show K-Means | 3 | 0.3944 |

The TV Show clustering model achieved a higher silhouette score than the Movie clustering model for the selected features.

## Business Insights

- Recent movies form the largest movie segment.
- Recent shorter movies represent another significant content segment.
- Classic movies form a smaller segment of the dataset.
- Recent TV Shows are divided into multi-genre and focused-genre segments.
- Classic TV Shows generally have more seasons than the recent TV Show segments.

These insights describe patterns in the available metadata and do not indicate actual audience popularity.

## Project Structure

```text
Netflix_Content_Success_Analytics/
│
├── Dataset(1).csv
├── Netflix_Content_Analysis.csv
├── Movie_Cluster_Insights.csv
├── TV_Show_Cluster_Insights.csv
├── Model_Evaluation.csv
│
├── Netflix_Movie_Clustering.pkl
├── Netflix_TV_Show_Clustering.pkl
├── Netflix_Feature_Information.pkl
│
├── Netflix_Content_Success_Analytics.ipynb
├── requirements.txt
└── README.md
```

## Installation

Install the required Python libraries:

```bash
pip install -r requirements.txt
```

## Execution

1. Open the Jupyter Notebook in Google Colab.
2. Upload the Netflix dataset.
3. Execute the notebook cells sequentially.
4. Perform data preprocessing and feature engineering.
5. Train the Movie and TV Show clustering models.
6. Generate business insights and visualizations.
7. Export the analysis results as CSV files.
8. Save the trained ML pipelines as PKL files.

## Limitations

- The dataset does not contain actual viewership or revenue information.
- The metadata-based success score is a manually defined analytical indicator.
- Clustering results depend on feature selection and the number of clusters.
- Movie duration is measured in minutes, whereas TV Show duration is measured in seasons.
- Cluster labels are identifiers, not popularity rankings.

## Future Enhancements

- Integrate actual audience engagement and viewing data.
- Explore additional clustering algorithms.
- Develop an interactive business intelligence dashboard.
- Improve automated content analytics.
- Deploy the ML pipeline as an application.

## Author

**Gokul K**

B.E. Artificial Intelligence and Data Science

Machine Learning Intern – Auspify Technologies