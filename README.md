# Flood Risk Visualisation and Analysis

## Project Overview

This project explores a dataset containing flood-related risk factors and a flood probability measure using Python. It applies exploratory data analysis (EDA), descriptive statistics and data visualisation to examine the dataset and illustrate patterns among its numerical variables.

The project uses pandas, NumPy, Matplotlib and Seaborn to inspect the data, generate summary statistics and create visualisations.

## Objectives

- Load and inspect the flood dataset.
- Examine the structure, data types and descriptive statistics.
- Summarise numerical variables.
- Visualise the distribution of a selected variable.
- Explore relationships between numerical variables.
- Compare distributions across numerical features.
- Present the analysis in a reproducible Python script.

## Dataset

**File:** `flood.csv`

The supplied dataset contains **50,000 rows and 21 columns**.

It includes 20 numerical variables describing flood-related factors and one outcome variable, `FloodProbability`.

Examples of the variables include:

- `MonsoonIntensity`
- `TopographyDrainage`
- `RiverManagement`
- `Deforestation`
- `Urbanization`
- `ClimateChange`
- `DamsQuality`
- `Siltation`
- `DrainageSystems`
- `CoastalVulnerability`
- `WetlandLoss`
- `InadequatePlanning`
- `FloodProbability`

The complete list of variables is available in the CSV file.

**Data provenance:** The original dataset publisher, source URL and licence have not yet been verified. Add those details when they are available.

## Technologies Used

- **Python** — programming language
- **pandas** — data loading and tabular analysis
- **NumPy** — numerical operations
- **Matplotlib** — chart creation
- **Seaborn** — statistical visualisation

## Analysis Workflow

### 1. Data loading and inspection

The script loads `flood.csv` into a pandas DataFrame and inspects the first rows, column information and descriptive statistics.

### 2. Numerical data selection

Numerical columns are selected automatically to support summary statistics and visualisation.

### 3. Descriptive statistics

The script generates descriptive summaries, including counts, means, standard deviations, minimums, quartiles and maximums.

### 4. Visualisations

The script generates and saves four plots:

| Plot | Purpose |
|---|---|
| `plot1_trend.png` | Displays the first numerical variable against the observation index |
| `plot2_scatter.png` | Explores the relationship between the first two numerical variables |
| `plot3_distribution.png` | Shows the distribution of the first numerical variable |
| `plot4_boxplot_rotated.png` | Compares distributions across numerical variables |

The charts are saved as PNG images at 300 DPI for clear presentation.

## Repository Structure

```text
flood-risk-visualisation-analysis/
├── README.md
├── final_visualisation_report.py
├── flood.csv
└── plots/
    ├── plot1_trend.png
    ├── plot2_scatter.png
    ├── plot3_distribution.png
    └── plot4_boxplot_rotated.png
```

The `plots/` folder represents the intended location for generated images. Create it and place the exported images there if you want to keep the repository organised.

## How to Run

### Using Google Colab

1. Open the Python script in Google Colab or copy its code into a notebook.
2. Upload `flood.csv` when prompted by the script.
3. Ensure the required libraries are available.
4. Run the cells or script in order.
5. Review the descriptive statistics and visualisations.
6. Download the generated PNG files if you want to include them in the repository.

### Required libraries

Install the main dependencies with:

```bash
pip install pandas numpy matplotlib seaborn
```

The supplied script uses `google.colab.files` for file upload, so that part is specific to Google Colab. When running locally, replace the upload code with a standard pandas file-loading statement, such as `pd.read_csv("flood.csv")`.

## Limitations

- The current visualisations use automatically selected numerical columns rather than explicitly chosen variables.
- The first chart plots observations against their row index; it should not be interpreted as a time trend because no time variable is specified in the script.
- The scatter plot examines only the first two numerical columns.
- The current script performs inspection and visualisation but does not implement a complete data-cleaning pipeline.
- Relationships shown in the charts do not establish causation.
- The meaning, units and provenance of the variables should be verified against the original dataset documentation before drawing substantive conclusions.

## Conclusion

This project provides an exploratory overview of a flood-related dataset through descriptive statistics and four visualisations. It demonstrates a basic Python workflow for inspecting numerical data, exploring distributions and examining relationships between variables.

Further work could include checking data quality, examining correlations with `FloodProbability`, selecting variables based on the research question and improving the interpretation of the visual results.

## Academic and Portfolio Use

This repository documents the code, dataset and visual outputs for a data analysis project. Findings should be interpreted in line with the source dataset's documentation and the limitations of the analysis.
