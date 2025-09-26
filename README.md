# NDD_x_meds
Repository for exploring NDD and medication associations in a hypothesis free manner

This repositiory contains notebooks for the paper MEDICATION EXPOSURE AND NEURODEGENERATIVE DISEASE RISK ACROSS NATIONAL BIOBANKS.

Notebooks to be used on the UK Biobank RAP platform have the prefix "UKB".  
Notebooks to be used on the All of Us Researchers Workbench have the prefix "AoU".

Files should be run in order -- pulling data first, then prepping/cleaning the files, then running the analyses.

# UKB
## Pulling data
* 01_UKB_make_case_controls.ipynb -- This notebooks pulls the data need to created case/control cohorts for Alzheimer's disesase, all-cause dementia, and Parkinson's disease.
* 01_UKB_pull_med_data.ipynb -- This notebook pulls and starts to clean the medication data.
* 06_UKB_pull_icd10_data.ipynb -- This notebook pulls the ICD10 codes we use as covariates.

## Prepping files
* 02_UKB_add_short_name_to_med_data.ipynb -- This notebook adds a "short name" to medications, allowing us to group medication with different names by their generic ingredients.
* 03_UKB_save_meds_as_individual_files.ipynb -- This notebook cleans drug data and saves a smaller csv file per each type of drug.
* 04_UKB_prep_med_df.ipynb -- This notebook merges the cases/controls, cleans the data, and creates the df used for the baseline cox analysis in table 1.
* 07_UKB_prep_df_with_icd10_APOE -- This notebook addes additional info, specifically ICD10 codes and APOE status, to create the df to be used for tables 2 and 4.
* 09_UKB_prep_df_table3.ipynb -- This notebooks adds high, med, low usage groupings to create the df to be used for table 3.

## Running regressions
* 05_UKB_baseline_cox_table1.ipynb
* 08_UKB_cox_table2_and_table4.ipynb
* 10_UKB_cox_high_low_table3.ipynb

# AoU
## Pulling data
* 01_AoU_pull_AD_cases.ipynb -- This notebook pulls Alzheimer's disease cases.
* 01_AoU_pull_DEM_cases.ipynb -- This notebook pulls all-cause dementia cases.
* 01_AoU_pull_PD_cases.ipnyb -- This notebook pulls Parkinson's disease cases.
* 02_AoU_pull_controls_60.ipynb -- This notebook pulls the controls for AoU.
* 02_AoU_death_drug_exposure_consent_dates.ipynb -- This notebook pulls death dates, a list of all participants with drug data, and consent dates for participants.
* 03_AoU_pull_drugs_and_clean_files.ipynb -- This notebook pulls and cleans drug data and saves a smaller csv file per each type of drug.
* 06_AoU_pull_APOE_status_V8.ipynb -- This notebook pulls the APOE status for each particiant from AoU's WGS data.
* 06_AoU_pull_icd10.ipynb -- This notebook pulls the ICD10 codes we use as covariates.

## Prepping files
* 04_AoU_prep_meds_df.ipynb -- This notebook merges the cases/controls, cleans the data, and creates the df used for the baseline cox analysis in table 1.
* 07_AoU_prep_df_with_ICD10_APOE.ipynb -- This notebook addes additional info, specifically ICD10 codes and APOE status, to create the df to be used for tables 2, 3, and 4.

## Running regressions
* 05_AoU_baseline_cox_table1.ipynb -- This notebook runs the regressions for table 1, using a previously created df.
* 08_AoU_cox_table2_and_table4.ipynb -- This notebook runs the regressions for table 2 and table 4.
* 09_AoU_cox_high_low_table3.ipynb -- This notebook runs the regressions for table 3.

Note -- currently in process of uploading notebooks
