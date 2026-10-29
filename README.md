# 🏥 Exploratory Data Analysis — Hospital Management System

### 🔎 Data Analysis | 🐍 Python | 🧹 Data Cleaning | 📊 Visualization | 🤖 Automated EDA

---

## 🌟 Project Overview

This project explores hospital management data through exploratory data analysis (EDA). It covers five datasets: appointments, billing, doctors, patients, and treatments.

The analysis uses Python to inspect the data, check for quality issues, summarize records, explore relationships, and create visualizations. Automated EDA tools are also used to generate additional dataset summaries and reports.

> 💡 **Project focus:** Understand the available hospital data and communicate patterns found in the records.

## 🎯 Project Objectives

- 🔍 Inspect the structure and contents of each dataset.
- 🧹 Identify missing values, duplicate rows, and data types that may need attention.
- 🛠️ Apply appropriate data-cleaning methods.
- 📊 Summarize records by category and numeric measure.
- 📉 Explore distributions, relationships, and potential outliers.
- 📈 Present analysis through charts and automated EDA reports.

## 🚀 Project Highlights

| Area | Description |
|---|---|
| 📂 Datasets | Appointments, billing, doctors, patients, and treatments |
| 🔍 Data inspection | Rows, columns, data types, and summary statistics |
| 🧹 Data quality | Missing-value, duplicate, and data-type checks |
| 📊 Analysis | Filtering, grouping, aggregation, and correlation |
| 📉 Outlier review | IQR and z-score methods |
| 📈 Visualization | Charts for exploring distributions and relationships |
| 🤖 Automated EDA | Sweetviz, D-Tale, YData Profiling, and AutoViz |
| 🐍 Language | Python |
| ☁️ Platform | Google Colab and Jupyter Notebook |

## 🛠️ Technologies and Tools

### 🐍 Programming and Data Analysis

- Python
- pandas
- NumPy

### 📊 Visualization

- Matplotlib
- Seaborn
- Plotly

### 🤖 Automated EDA

- Sweetviz
- D-Tale
- YData Profiling
- AutoViz

### ☁️ Platforms

- Google Colab
- Jupyter Notebook
- GitHub

## 📁 Dataset Information

The project uses five CSV files:

| File | Description |
|---|---|
| `appointments.csv` | Appointment records and related details |
| `billing.csv` | Billing and payment records |
| `doctors.csv` | Doctor information |
| `patients.csv` | Patient information |
| `treatments.csv` | Treatment information |

The exact fields available for analysis depend on the columns in each CSV file.

## 📓 Project Notebooks

- [🏥 Hospital Management EDA](EDA_Hospital_management_system.ipynb)
- [🤖 Automatic Visualization Tools](AUTOMATIC_TOOLS_HMS.ipynb)

The notebook names above are based on the files shown in the repository. Update the links if the filenames differ.

## 🔄 EDA Workflow

```text
📂 Load the datasets
        ↓
🔍 Inspect rows, columns, and data types
        ↓
🧹 Check data quality
        ↓
🛠️ Clean data where appropriate
        ↓
📊 Summarize and analyze
        ↓
📉 Review potential outliers
        ↓
📈 Create visualizations
        ↓
🤖 Generate automated EDA reports
        ↓
💡 Summarize findings
```

## 🔍 Exploratory Data Analysis

### 1️⃣ Inspect the datasets

Pandas methods help inspect sample records, dimensions, column names, data types, non-missing counts, and summary statistics.

```python
df.head()
df.tail()
df.info()
df.describe(include="all")
df.columns
df.shape
df.size
df.count()
```

| Method | Purpose |
|---|---|
| `head()` | Displays the first rows |
| `tail()` | Displays the last rows |
| `info()` | Shows column types and non-missing counts |
| `describe()` | Summarizes column values |
| `columns` | Lists column names |
| `shape` | Returns the number of rows and columns |
| `size` | Returns the total number of data cells |
| `count()` | Counts non-missing values |

### 2️⃣ Check data quality

The datasets can be checked for missing values, duplicate rows, data types, and numeric ranges.

```python
df.isna().sum()
df.duplicated().sum()
df.dtypes
df.min(numeric_only=True)
df.max(numeric_only=True)
```

### 3️⃣ Clean the data

Cleaning methods should be chosen based on the meaning of each column:

- 🗑️ Remove rows or columns only when their removal is appropriate.
- 🔢 Fill missing values with a constant when a meaningful default is available.
- 📐 Use the mean or median for suitable numeric columns.
- 🏷️ Use the mode for suitable categorical columns.
- ⬆️ Use forward fill or backward fill only when neighboring rows are meaningfully related.
- 🔄 Use interpolation for ordered numeric data when estimating between nearby values makes sense.
- 📅 Convert dates, times, and other fields to suitable data types when needed.

Cleaning decisions can affect analysis results, so they should be reviewed and documented.

### 4️⃣ Analyze and summarize

Filtering, grouping, aggregation, and correlation can help summarize the datasets and explore relationships.

```python
df.groupby("category").size()

df["numeric_column"].agg(
    ["count", "min", "max", "mean", "std"]
)

df.corr(numeric_only=True)
```

Replace the example column names with names that exist in the relevant CSV file.

### 5️⃣ Review potential outliers

The IQR and z-score methods can flag unusual numeric values for further review. A flagged value is not automatically an error; check it in context before changing or removing it.

### 6️⃣ Visualize the data

Charts can help explore counts, distributions, trends, and relationships. Depending on the data, visualizations may include:

- 📊 Bar charts and count plots
- 📉 Histograms and box plots
- 📈 Line and area charts
- 🌡️ Heatmaps
- 🔵 Scatterplots and pairplots
- 🍩 Donut charts
- 🖱️ Interactive Plotly charts

Choose charts that fit the columns and analysis question.

## 🤖 Automated EDA Tools

Automated EDA tools generate summaries and visual reports that support manual analysis.

| Tool | Purpose |
|---|---|
| **D-Tale** | Interactive exploration of a DataFrame |
| **YData Profiling** | Dataset summaries, distributions, and data-quality reports |
| **AutoViz** | Automated chart generation |
| **Sweetviz** | Visual dataset analysis and comparison reports |

Install the libraries in a notebook cell if needed:

```python
%pip install dtale ydata-profiling autoviz sweetviz
```

## ▶️ How to Run

### ☁️ Google Colab

1. Open one of the project notebooks.
2. Upload the five CSV files to the Colab session or connect Google Drive.
3. Check that the file paths in the notebook match the CSV locations.
4. Run the notebook cells in order.
5. Review the analysis, charts, and generated reports.

### 💻 Local Environment

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn plotly
pip install dtale ydata-profiling autoviz sweetviz
```

Place the notebooks and CSV files in the appropriate project folders, update the file paths, and open the notebook in Jupyter.

## 📊 Results and Findings

Add a summary of your confirmed findings here after running the notebooks. Possible topics include appointment counts by status, billing summaries, patient distributions, doctor specialties, and treatment frequencies.

Include only findings supported by the data and your analysis.

## ⚠️ Limitations and Data Privacy

- The analysis depends on the accuracy and completeness of the supplied CSV files.
- Available columns may differ from examples in the notebooks.
- Missing-value and outlier methods require judgment and may affect results.
- Correlation indicates association; it does not establish cause and effect.
- 🔒 Do not publish private or identifiable patient information in a public repository. Use approved, anonymized, or synthetic data when sharing the project.

## 🧠 Learning Outcomes

This project provides practice with:

- ✅ Exploratory data analysis
- ✅ Data inspection and cleaning
- ✅ Missing-value and duplicate checks
- ✅ Filtering, grouping, and aggregation with pandas
- ✅ Descriptive statistics and correlation
- ✅ Potential outlier detection
- ✅ Data visualization
- ✅ Automated EDA tools
- ✅ Clear communication of findings

## 👩‍💻 Author

**Rama Lakshmi Neerukonda**

---

🙏 Thank you for visiting this project. Explore the notebooks to review the analysis and visualizations.
