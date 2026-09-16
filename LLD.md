# Low-Level Design (LLD)

## 1. Notebook Structure

The main implementation is contained in:

```text
Netflix_EDA.ipynb
```

The notebook should follow this logical order:

```text
1. Import Libraries
2. Load Dataset
3. Dataset Inspection
4. Data Cleaning
5. Exploratory Data Analysis
6. Visualization
7. Key Insights
```

## 2. Library Imports

The analysis uses:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

## 3. Data Loading

The Netflix Titles CSV file is loaded into a Pandas DataFrame.

Conceptually:

```python
df = pd.read_csv("data/netflix_titles.csv")
```

## 4. Dataset Structure

The dataset contains 8,807 rows and 12 columns:

```text
show_id
type
title
director
cast
country
date_added
release_year
rating
duration
listed_in
description
```

## 5. Data Inspection

Typical inspection operations include:

```python
df.shape
df.columns
df.head()
df.info()
df.isnull().sum()
```

These operations help understand the dataset and identify missing values before analysis.

## 6. Data Cleaning

Relevant missing values are handled before analysis.

The project documentation specifies handling missing country values and removing rows where rating data is required for the rating analysis.

## 7. Analysis Modules

### 7.1 Movies vs TV Shows
Group records by the `type` column and visualize the distribution.

### 7.2 Country Analysis
Analyze the `country` field and identify the countries contributing the most titles.

### 7.3 Release Year Analysis
Group titles by `release_year` and visualize changes in content releases over time.

### 7.4 Rating Analysis
Group records by `rating` and visualize the rating distribution.

### 7.5 Genre Analysis
Use the `listed_in` field to identify and visualize the most common genres.

## 8. Output Charts

The implementation produces:
- `movies_vs_tvshows.png`
- `top10_countries.png`
- `release_year_trend.png`
- `ratings_distribution.png`
- `top_genres.png`

## 9. Execution

Install dependencies:

```bash
pip install -r requirements.txt
```

Start Jupyter:

```bash
jupyter notebook
```

Open:

```text
Netflix_EDA.ipynb
```

and run the notebook cells.

## 10. Project Structure

```text
Netflix-Data-Analysis/
├── data/
│   └── netflix_titles.csv
├── images/
│   ├── movies_vs_tvshows.png
│   ├── top10_countries.png
│   ├── release_year_trend.png
│   ├── ratings_distribution.png
│   └── top_genres.png
├── Netflix_EDA.ipynb
├── HLD.md
├── LLD.md
├── PRD.md
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```
