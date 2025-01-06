# Analysis

This folder contains the analysis files for the **US Homicides (1976-2024)** project. The analyses focus on exploring/visualizing the data and building a machine learning model to predict whether a homicide case will be solved.

## File Descriptions
- **`us_homicide_data.qmd`**: A Quarto document containing the full code and narrative for the analysis. This file is intended for those with R and RStudio installed who wish to reproduce or adapt the analysis.
- **`us_homicide_data.html`**: A rendered HTML file of the Quarto document, viewable in any web browser. This is a static version of the analysis, including both code and output, for easy sharing.

## Reproducibility
### Requirements
To reproduce the analysis:
1. Install R (version 4.0 or higher) and RStudio.
2. Install the necessary R packages listed in the `analysis.qmd` file.
3. Open the `.qmd` file in RStudio and execute the code.

### Viewing Only
If you do not wish to reproduce the analysis, simply open the `.html` file in your web browser to explore the code, visualizations, and results.

## Key Highlights
The analysis includes:
- **Exploratory Data Analysis (EDA)**: Visualizations and summaries of homicide data across time, demographics, and other features.
- **Feature Selection**: Identification of important predictors for case solvability.
- **Machine Learning**: A random forest model to predict case status (unsolved vs. solved).
