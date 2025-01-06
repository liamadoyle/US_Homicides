# Predicting Unsolved Homicides (USA, 1976-2024)

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset Description](#dataset-description)
3. [Methods and Approach](#methods-and-approach)
4. [Key Findings](#key-findings)
5. [Limitations and Future Work](#limitations-and-future-work)
6. [Repository Structure](#repository-structure)
7. [Technical Skills Demonstrated](#technical-skills-demonstrated)

## Project Overview

This project explores and models a dataset of nearly 900,000 homicide cases in the United States. The goal was to create a machine learning model capable of predicting the future case status (solved or unsolved) based on features available at the start of an investigation.

## Dataset Description

The dataset used for this project was provided by the Murder Accountability Project (MAP; https://www.murderdata.org/), a non-profit dedicated to cataloging and tracking unsolved homicides in the United States of America. This dataset is comprised of case-level data for 894,637 homicides between 1976 to 2024. 

The dataset includes case-level data such as:
- Victim demographics (e.g., sex, age, race)
- Incident details (e.g., weapon used, location)
- Case status (solved/unsolved)

Through Freedom of Information Act requests to the FBI, this dataset is periodically updated to (a) add new cases and (b) update the case details of existing cases. The current project used the October 2024 snapshot of the dataset. 

## Methods and Approach

1. **Data Preprocessing and Cleaning**:
   - Organized and cleaned data using Tidyverse packages.
2. **Exploratory Data Analysis**:
   - Used summary statistics and visualizations to examine the structure and characteristics of the data.
3. **Feature Selection**:
   - Selected features (e.g., murder weapon, victim sex, location) available at the outset of an investigation.
4. **Modelling**:
   - Built and evaluated a random forest model to predict case status (i.e., unsolved vs. solved).
  
## Key Findings

Several key findings emerged from this project. First, the results of the random forest model indicated that certain case characteristics (e.g., the circumstance of the homicide) had more predictive value than other case characteristics (e.g., the number of victims). While no causal mechanism can be discerned from this analysis, these results highlight what may be the most valuable details for investigators to identify when investigating a homicide.

Second, preliminary results suggest that predictive algorithms such as random forest models could assist law enforcement agencies in allocating resources more effectively. As the features included in the algorithm were selected to represent case details commonly available to law enforcement officials at the outset of an investigation (e.g., victim age, murder weapon), law enforcement agencies could use a predictive algorithm such as this to generate empirical predictions of whether a homicide case will be solved in the future. For instance, law enforcement officials might choose to allocate a greater amount of resources to homicide cases that are predicted to remain unsolved. Use of a predictive algorithm would provide an evidence-based foundation for these kinds of decisions. 

In addition, the American policing system consists of various agencies with overlapping jurisdictions. These agencies also differ in the amounts of resources that they can access (e.g., manpower, technology). Occasionally, smaller law enforcement agencies (e.g., sheriffs, tribal policing agencies) must request aid from larger law enforcement agencies (e.g., state law enforcement, federal bodies such as the FBI) in order to properly investigate crimes. In this case, a machine learning algorithm would provide another evidence-based foundation for such requests and enable smaller law enforcement agencies to quantitatively justify their requests for aid. Given the scarcity of resources (even at higher levels), this would also help larger law enforcement agencies make decisions as to how to allocate resources to smaller law enforcement agencies.

## Limitations and Future Work

It should be noted that this project was designed to demonstrate the potential applicability of this approach rather than provide specific feedback on a given homicide case. While I do believe that this project is conceptually useful, it should be noted that there are some limitations. For instance, I did not have access to key information such as the dates when homicide cases were solved. With this information, I would have been able to create a date measure that indicates how long cases remained unsolved. In addition, there were likely biases inherent in the  dataset due to reporting inconsistencies. While there was relatively little missing data, the assignment of certain values (e.g., the circumstance of the murder) requires a degree of subjectivity on the behalf of investigators. With the available information, it is difficult to determine the interrater reliability of such features. In sum, this project represents a sort of "proof of concept" rather than a final product. 

## Repository Structure

- `data/`: Contains web links to the dataset and related documentation.
- `analysis/`: Includes analysis scripts (`.qmd`) and rendered outputs (`.html`).

## Technical Skills Demonstrated

- **R**: For data analysis, visualization, and model development.
- **Quarto**: For report generation and sharing insights.
- **Data Processing and Feature Engineering**: Used `dplyr` and other `tidyverse` packages to clean/process the data and select/transform features.
- **Visualization**: Used `gt` and `ggplot2` for creating professional tables and plots.
- **Machine Learning**: Used the `tidymodels` workflow to build and evaluate a random forest model.


