# High-Level Design (HLD)

## 1. System Overview
Netflix Data Analysis is a standalone data-analysis application implemented as a Jupyter Notebook. The system follows a simple pipeline:

**Dataset → Data Loading → Data Cleaning → Exploratory Analysis → Visualization → Insights**

## 2. Architecture

```text
+-----------------------+
| Netflix Titles Dataset|
|       (CSV)           |
+-----------+-----------+
            |
            v
+-----------------------+
| Data Loading          |
| Pandas read_csv()     |
+-----------+-----------+
            |
            v
+-----------------------+
| Data Inspection       |
| Shape, columns, nulls |
+-----------+-----------+
            |
            v
+-----------------------+
| Data Cleaning         |
| Missing-value handling|
+-----------+-----------+
            |
            v
+-----------------------+
| Exploratory Data      |
| Analysis              |
+-----------+-----------+
            |
            v
+-----------------------+
| Matplotlib            |
| Visualizations        |
+-----------+-----------+
            |
            v
+-----------------------+
| Findings / Insights   |
+-----------------------+
```

## 3. Main Components

### 3.1 Data Source
The system uses the Netflix Titles dataset obtained from Kaggle.

### 3.2 Data Processing Layer
Pandas and NumPy are used to:
- Load the dataset.
- Inspect rows and columns.
- Identify missing values.
- Prepare data for analysis.

### 3.3 Analysis Layer
The analysis focuses on:
- Content type
- Country
- Release year
- Rating
- Genre

### 3.4 Visualization Layer
Matplotlib is used to create charts for the major findings.

### 3.5 Presentation Layer
The Jupyter Notebook presents the analysis, charts, and conclusions in an interactive sequence.

## 4. Technology Stack
| Layer | Technology |
|---|---|
| Language | Python |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib |
| Development Environment | Jupyter Notebook |
| Dataset | Netflix Titles Dataset |

## 5. Data Flow
1. Read the CSV dataset.
2. Store the dataset in a Pandas DataFrame.
3. Inspect its structure and missing values.
4. Clean/preprocess relevant fields.
5. Perform aggregations and exploratory analysis.
6. Generate visualizations.
7. Interpret and document the results.

## 6. Non-Functional Considerations
- The notebook should be reproducible.
- Analysis should use clear and understandable visualizations.
- Dependencies should be documented in `requirements.txt`.
- The project should remain simple enough to run locally with Jupyter Notebook.
