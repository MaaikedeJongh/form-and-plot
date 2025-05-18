# Form and Plot
## Exploring the role of genre, author gender and quality ratings in narrative arcs in Dutch-language novels

This repository contains the scripts and data used in a study to analyze narrative structures in Dutch-language novels and compare them with English-language literature. The research leverages the framework proposed by Boyd et al. (2020) to explore trends in Staging, Plot Progression, and Cognitive Tension across a corpus of 401 Dutch novels. The study investigates whether narrative trends identified in English-language literature also emerge in Dutch novels. Key factors such as genre, author gender, literary quality, and reader-assigned quality are examined to understand their influence on narrative arcs. The findings highlight notable differences, including the pronounced impact of the Romantic genre and gender-related variations in narrative structure.

## Repository Contents

### Scripts

#### 1. `Trend Analysis.ipynb`
This script performs statistical analysis and visualizations to explore normalized metrics (Staging, Plot Progression, Cognitive Tension) across various segmentations of the novels. 

**Key Features:**
- ANOVA and partial eta squared analysis for trends by relative segment.
- Linear and quadratic model fitting to assess relationships between metrics and narrative progression.
- 10x10 cross-validation to evaluate model robustness.
- Combined visualizations for all segmentation methods.

**Results:**
- CSV files summarizing statistical analyses (e.g., ANOVA results, R-squared values, cross-validation scores).
- Combined visualizations saved as PNG files.

#### 2. `Factor Analysis.ipynb`
This script applies Generalized Linear Models (GLM) to study how factors such as genre, gender, literary quality, and reader-assigned quality impact narrative metrics.

**Key Features:**
- GLM analysis for multiple dependent variables (Staging, Plot Progression, Cognitive Tension).
- Separate visualizations for each dataset and dependent variable.
- Organized folder structure for saving results.

**Results:**
- Summary CSV file with statistical metrics (AIC, BIC, Pseudo R-squared, coefficients).
- Visualizations showing the relationship between narrative metrics and the examined factors.

#### 3. `Casestudies.ipynb`
This script identifies books that best represent the average trendlines for specific groups in normalized metrics (e.g., Staging, Plot Progression). It visualizes comparisons between individual book trends and group trends.

**Key Features:**
- Filters dataset by attributes such as Gender and Genre to identify specific groups.
- Fits quadratic models using GLM for group and individual book trends.
- Identifies books closest to group trends based on Mean Squared Error (MSE).
- Generates visual comparisons between individual books and group trends.

**Results:**
- PNG files showing group trends and individual book comparisons, saved with descriptive filenames.
- Organized folder structure for results under `Results Casestudies_YYYY-MM-DD`.

### Data
- Input data files are in CSV format, structured by segmentation methods (e.g., 5 segments, 10 segments, 500-word segments, 1000-word segments).
- Normalized metrics include `Staging_z`, `PlotProgression_z`, and `CognitiveTension_z`.

### Results
- Generated results are saved in directories named by execution date (e.g., `Results Trend Analysis_YYYY-MM-DD`, `Results Factor Analysis_YYYY-MM-DD`, or `Results Casestudies_YYYY-MM-DD`).
- Subdirectories categorize results by segmentation method, narrative metric, or group comparisons.

## Dependencies
The scripts require the following Python libraries:
- `pandas`
- `numpy`
- `statsmodels`
- `seaborn`
- `matplotlib`
- `sklearn`
- `re`

Install the dependencies using:
```bash
pip install pandas numpy statsmodels seaborn matplotlib scikit-learn
```

## Usage Instructions

1. **Prepare Data:** The input data files are in CSV format and placed in the appropriate directory. The filenames and formats should align with those specified in the `datasets` list in the scripts.

2. **Run Scripts:**
   - For trend analysis, execute `Trend Analysis.ipynb` to generate statistical summaries and combined visualizations.
   - For factor analysis, run `Factor Analysis.ipynb` to evaluate the influence of literary factors on narrative metrics.
   - For case studies, use `Casestudies.ipynb` to identify representative books and generate visual comparisons.

3. **Access Results:**
   - Statistical results and visualizations are saved in organized directories under `Results Trend Analysis_YYYY-MM-DD`, `Results Factor Analysis_YYYY-MM-DD`, or `Results Casestudies_YYYY-MM-DD`.
   - Check the summary CSV files for key statistical insights.

