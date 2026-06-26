# pca-player-selection

# Cricket Player Performance Analysis Using Principal Component Analysis (PCA)

## Overview

This project demonstrates how **Principal Component Analysis (PCA)** can be applied to evaluate cricket player performance using multiple statistical metrics. Instead of relying on a single metric such as runs or wickets, the project combines several performance indicators into a composite score to rank players objectively.

The project performs data preprocessing, feature standardization, dimensionality reduction using PCA, and player ranking based on calculated composite scores.

This implementation serves as a practical example of applying Machine Learning techniques to sports analytics and demonstrates how dimensionality reduction can assist in decision-making.

---

# Problem Statement

Evaluating a cricket player's overall performance cannot be done accurately using only one statistic.

For example,

* A batsman may have high runs but a low strike rate.
* A bowler may have many wickets but a poor bowling average.
* Some players perform consistently across multiple metrics.

The objective of this project is to combine multiple performance indicators into a lower-dimensional representation using Principal Component Analysis (PCA) and rank players based on their overall contribution.

---

# Objectives

The project aims to:

* Analyze cricket player statistics.
* Standardize numerical features.
* Apply Principal Component Analysis.
* Reduce multiple correlated variables into principal components.
* Calculate composite performance scores.
* Rank players objectively.
* Identify top-performing players.

---

# Dataset

The sample dataset contains performance statistics for 10 cricket players.

### Features

| Feature     | Description          |
| ----------- | -------------------- |
| Player      | Player Name          |
| Strike_Rate | Batting Strike Rate  |
| Average     | Player Average       |
| Runs        | Total Runs Scored    |
| Wickets     | Total Wickets Taken  |
| Matches     | Total Matches Played |

---

# Project Workflow

```
Raw Cricket Data
        │
        ▼
Create Pandas DataFrame
        │
        ▼
Feature Selection
        │
        ▼
Standardize Features
        │
        ▼
Principal Component Analysis (PCA)
        │
        ▼
Generate Principal Components
        │
        ▼
Calculate Composite Scores
        │
        ▼
Rank Players
        │
        ▼
Identify Best Performers
```

---

# Technologies Used

* Python
* NumPy
* Pandas
* Scikit-learn
* Matplotlib

---

# Machine Learning Technique

## Principal Component Analysis (PCA)

Principal Component Analysis is an unsupervised Machine Learning algorithm used for:

* Dimensionality Reduction
* Feature Extraction
* Removing Redundancy
* Identifying Hidden Patterns
* Data Visualization

Instead of analyzing every feature independently, PCA transforms correlated variables into a smaller number of principal components while preserving most of the variance present in the data.

---

# Data Preprocessing

Before applying PCA, the dataset is standardized because the features are measured on different scales.

Standardization transforms each feature using:

```
Standardized Value = (Value - Mean) / Standard Deviation
```

This ensures that every feature contributes equally during PCA.

---

# PCA Implementation

The project reduces five original performance metrics into **two principal components**.

The generated principal components summarize the majority of information present in the original dataset while reducing dimensionality.

Example output:

| Principal Component 1 | Principal Component 2 | Player      |
| --------------------- | --------------------- | ----------- |
| PC1                   | PC2                   | Player Name |

---

# Composite Score Calculation

A composite score is calculated for every player using:

```
Composite Score =
|Principal Component 1|
+
|Principal Component 2|
```

Players with larger composite scores are considered better overall performers according to the selected metrics.

---

# Player Ranking

Players are ranked based on their composite scores.

The player with the highest score receives Rank 1.

The final ranking table includes:

* Player Name
* Composite Score
* Rank

---

# Visualization

The project visualizes player performance using PCA scatter plots.

The visualization helps identify:

* Similar player profiles
* Outliers
* Performance clusters
* Separation between high and low performers

---

# Project Structure

```
Cricket-PCA-Analysis/
│
├── Cricket_Player_Analysis.ipynb
├── README.md
├── requirements.txt
└── images/
    └── pca_plot.png
```

---

# Installation

Clone the repository

```bash
git clone https://github.com/your-username/Cricket-PCA-Analysis.git
```

Move into the project directory

```bash
cd Cricket-PCA-Analysis
```

Install the dependencies

```bash
pip install -r requirements.txt
```

Run the notebook

```bash
jupyter notebook
```

---

# Requirements

```
numpy
pandas
matplotlib
scikit-learn
```

Install using

```bash
pip install numpy pandas matplotlib scikit-learn
```

---

# Sample Output

The project produces:

* Standardized Dataset
* Principal Components
* Composite Scores
* Ranked Players
* PCA Visualization

Example Ranking

| Rank | Player  | Composite Score |
| ---- | ------- | --------------- |
| 1    | Player9 | Highest Score   |
| 2    | Player4 | Second Highest  |
| 3    | Player5 | Third Highest   |

---

# Key Learning Outcomes

This project demonstrates:

* Data preprocessing
* Feature scaling
* Principal Component Analysis
* Dimensionality reduction
* Sports analytics
* Composite score calculation
* Data visualization
* Ranking based on statistical analysis

---

# Future Improvements

Potential enhancements include:

* Use a real-world cricket dataset.
* Analyze international players.
* Add batting and bowling statistics separately.
* Compare PCA with clustering algorithms.
* Build an interactive dashboard using Streamlit.
* Deploy the application on the cloud.
* Support IPL, ODI, Test, and T20 formats independently.

---

# Applications

This project can be applied in:

* Sports Analytics
* Cricket Performance Evaluation
* Player Selection
* Team Strategy Analysis
* Machine Learning Education
* Data Science Portfolio Projects

---

# Conclusion

This project demonstrates how Principal Component Analysis can simplify the evaluation of cricket player performance by reducing multiple statistical features into meaningful principal components. By combining these components into a composite score, the analysis provides an objective approach to ranking players and identifying top performers based on overall contribution rather than a single metric.

The project showcases the practical application of data preprocessing, dimensionality reduction, statistical analysis, and visualization techniques, making it a valuable example of applying Machine Learning concepts to real-world sports analytics.
