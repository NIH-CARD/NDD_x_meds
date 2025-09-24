# NDD_x_meds
Repository for exploring NDD and medication associations in a hypothesis free manner

This repositiory contains notebooks for the paper MEDICATION EXPOSURE AND NEURODEGENERATIVE DISEASE RISK ACROSS NATIONAL BIOBANKS.

Notebooks to be used on the UK Biobank RAP platform have the prefix "UKB".  
Notebooks to be used on the All of Us Researchers Workbench have the prefix "AoU".

Files should be run in order -- pulling data first, then prepping/cleaning the files, then running the analyses.

# Pulling data

## Pulling NDD cases:  
* 01_AoU_pull_AD_cases.ipynb  
* 01_AoU_pull_DEM_cases.ipynb  
* 01_AoU_pull_PD_cases.ipnyb

## Pulling control data:
* 02_AoU_pull_controls_60.ipynb

## Pulling other data types  
* 02_AoU_death_drug-exposure_consent_dates.ipynb -- This file pulls death dates, a list of all participants with drug data, and consent dates for participants.
* 03_AoU_pull_drugs_and_clean_files.ipynb -- This file pulls and cleans drug data and saves a smaller csv file per each type of drug.
* 06_AoU_pull_APOE_status_V8.ipynb -- This file pulls the APOE status for each particiant from AoU's WGS data.
* 06_AoU_pull_icd10.ipynb -- This file pulls the ICD10 codes we use as covariates.

# Prepping files -- to be run after pulling the data
* 04_AoU_prep_meds_df.ipynb -- This file merged the cases/controls, cleans the data, and creates the df used for the baseline cox analysis in table 1.
* 07_AoU_prep_df_with_ICD10_APOE.ipynb -- This files addes additional info, specifically ICD10 codes and APOE status, to the baseline df.

# Running regressions and creating tables -- to be run after completing all previous steps
* 05_AoU_baseline_cox_table1.ipynb -- This notebook runs the regressions for table 1, using a previously created df.
* 08_AoU_cox_table2_and_table4.ipynb -- This notebook runs the regressions for table 2 and table 4.
* 09_AoU_cox_high_low_table3.ipynb -- This notebook runs the regressions for table 3.

Note -- currently in process of uploading notebooks
