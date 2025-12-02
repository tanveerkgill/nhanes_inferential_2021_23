# NHANES Inferential Analysis 2021–2023

This repository contains my inferential statistics project using NHANES 2021–2023 data.  
All analysis is done in the Jupyter/Colab notebook `nhanes_inferential_2021_23.ipynb`.

## Data

The analysis uses selected variables from the NHANES 2021–2023 cycles, including:

- DMDMARTZ – Marital status (recoded to married vs not married)
- DMDEDUC2 – Education level (recoded to bachelor’s degree or higher vs less than bachelor’s)
- RIDAGEYR – Age in years
- BPXOSY3 – Systolic blood pressure
- PAD680 – Minutes of sedentary behavior (cleaned: removed 7777, 9999, and missing)
- WHD020 – Self-reported weight (cleaned: removed 7777, 9999, and missing)

## Analyses

The notebook is organized by question:

1. **Marital status vs education (association)**
   - Question: Is there an association between marital status and education level?
   - Variables: DMDMARTZ (recoded), DMDEDUC2 (recoded)
   - Method: Chi-square test of independence
   - Output: Contingency table and chi-square results, plus a short interpretation.

2. **Sedentary time by marital status**
   - Question: Is there a difference in mean sedentary behavior time between married and not married participants?
   - Variables: DMDMARTZ (recoded), PAD680 (cleaned)
   - Method: Two-sample t-test (or appropriate alternative, depending on assumptions)
   - Output: Descriptive stats, visualization (e.g., boxplot), and interpretation.

3. **Effects of age and marital status on systolic blood pressure**
   - Question: How do age and marital status affect systolic blood pressure?
   - Variables: RIDAGEYR, DMDMARTZ (recoded), BPXOSY3
   - Method: Regression or ANOVA-style model including age and marital status
   - Output: Model summary and brief explanation of effects.

4. **Correlation between weight and sedentary time**
   - Question: Is there a correlation between self-reported weight and minutes of sedentary behavior?
   - Variables: WHD020 (cleaned), PAD680 (cleaned)
   - Method: Correlation analysis (Pearson or Spearman)
   - Output: Correlation coefficient, scatterplot, and interpretation.

5. **Creative question**
   - Question: [Briefly state your custom question here.]
   - Variables: [List variables used.]
   - Method: [Chi-square, t-test, ANOVA, or correlation.]
   - Output: Summary of results and interpretation.

## How to Run

1. Open the notebook (`nhanes_inferential_2021_23.ipynb`) in Google Colab or Jupyter.
2. Run the cells from top to bottom to:
   - Load and clean the NHANES data
   - Recode variables
   - Perform each of the five analyses
   - View tables, plots, and written summaries
