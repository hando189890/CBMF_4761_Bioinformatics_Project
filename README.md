# COMS 4761 Final Project - ReadMe

## Name and Uni:
- Dongbing Han, dh3071
- Shanshan Gong, sg3445
- Chengyu Wang, cw3512

## Submitted Files:
- Github Links: [CBMF_4761_Bioinformatics_Project](https://github.com/hando189890/CBMF_4761_Bioinformatics_Project)
- `Data_Visualization_&_Classic_Regression.ipynb`: This notebook focuses on data visualization and implements classical regression methods for predicting cancer survival. The notebook is necessary for processing data, training, and testing with a survival model.
- `survive-model.ipynb`: This notebook is utilized to select the most significant and impactful genetic attributes using the Cox survival model. It also measures the AUC metrics for 3 different types of input.
- `Model and Results - Genetic Attributes.ipynb`: This script is dedicated to training and testing with the Univariate Cox Regression for features selection, Multivariate Cox Regression to generate the risk score stratification which predicted patients’ survival, Kaplan-Meier method and Log-Rank test to show statistical difference in clinical attributes like the 3-gene classifier subtype and estrogen receptor status between high and low-risk groups.
- `data.csv`: sample input
- CBMF_4761_Bioinformatics_Final_Report.pdf

## Description of the METABRIC Dataset:
- **Link:** [METABRIC Dataset](https://www.kaggle.com/datasets/raghadalharbi/breast-cancer-gene-expression-profiles-metabric)
- **Description:** METABRIC (Molecular Taxonomy of Breast Cancer International Consortium) is a comprehensive dataset containing genomic and clinical data from breast cancer patients. It encompasses gene expression profiles, DNA alterations, methylation patterns, and outcomes. Researchers utilize METABRIC to investigate breast cancer subtypes, prognostic markers, and predictive models for patient outcomes.

## Compilation Instructions: 
Not Applicable, please compile and run `.ipynb` files directly.

## Testing Procedure:
- The analysis begins by fitting a Cox Proportional Hazards Model (CoxPH) using the `lifelines` library which is widely used in survival analysis to assess the relationship between covariates and survival time.
- First genes significantly associated with breast cancer survival were identified through Univariate Cox regression analysis.
- Subsequently, a risk score is calculated for each patient based on their genetic attribute expression values and the coefficients obtained from the Multivariate Cox model. This risk score serves as an indicator of the likelihood of experiencing the event of interest, in this case, overall survival.
- To visualize the survival probabilities of these risk groups over time, Kaplan-Meier survival curves are plotted. This step allows for a clear comparison of survival outcomes between high-risk and low-risk groups.
- Moving on to the analysis of clinical data, the project separates clinical variables from genetic data. Categorical variables within the clinical dataset are then subjected to analysis using the chi-square test. This test evaluates whether there is a significant association between categorical clinical variables and the risk group assigned based on the Cox model. Significant p-values from this analysis are visualized using a bar graph, providing insights into which clinical variables may be predictive of the risk group.
- Finally, we measure time-dependent AUC metrics for different types of model input, namely mRNA data alone, clinical data and mRNA data, and clinical data alone. The outcome is plotted in a months/AUC-score graph.

## Execution on Large Files: 
Not Applicable

## Parameters: 
Not Applicable, please refer to code detail in `.ipynb` files.

## System Requirements: 
- Python 3.10 with TPU in Google Colab

## Selective Required Libraries: 
- Scikit-survival
- Lifelines
- Statsmodels
- Pandas
- Numpy
- Matplotlib
- Scipy
- Pytorch




