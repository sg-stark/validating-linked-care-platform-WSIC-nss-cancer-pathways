Validating a Linked Primary–Secondary Care Data Platform for Non-Specific Cancer Symptom Pathways

This repository contains the R and SQL analysis code supporting the study:

Gupta S, Alied M, Rafiq M, et al. Validating a linked primary–secondary care data platform for analysis of non-specific cancer symptom pathways: a retrospective study. npj Digital Public Health. 2026;1:34.
https://doi.org/10.1038/s44482-026-00040-8

Overview

Patients referred to Rapid Diagnostic Centres (RDCs) with non-specific symptoms (NSS) may have complex diagnostic pathways that are difficult to reconstruct using individual healthcare datasets.

This retrospective study evaluated whether the Whole Systems Integrated Care (WSIC) linked primary–secondary care data platform could be used to reconstruct and characterise diagnostic pathways for patients referred to an RDC.

The study included 2,021 patients referred to a London RDC between November 2021 and December 2024 whose records could be linked to WSIC primary-care data.

The analysis examined:

* demographic and clinical characteristics
* non-specific symptoms and symptom trajectories
* comorbidities and frailty
* smoking and alcohol status
* laboratory investigations and abnormal results
* primary-care healthcare utilisation
* prescribing patterns
* cancer and non-cancer diagnostic outcomes
* longitudinal follow-up following RDC referral

The linked dataset enabled reconstruction of longitudinal symptom, investigation, prescribing and healthcare-contact histories that were not available from the RDC dataset alone. The study found substantially greater completeness for several clinical and lifestyle variables in WSIC compared with the standalone RDC records. (Nature)

Repository contents

File	Description
rdc_analysis_clean.R	R code used for data processing, statistical analysis and generation of study outputs
SQL script_submission copy.txt	SQL code used for data extraction and preparation within the WSIC Secure Data Environment
README.md	Description of the study, data governance, code and reproducibility information

Analysis environment

The statistical analyses were conducted in R version 4.4.1 within the WSIC Secure Data Environment.

SQL was used for data extraction and preparation.

The analysis included descriptive statistics, temporal analyses and regression modelling, including Poisson, logistic and Cox regression models, as described in the published manuscript. (Nature)

Data availability and governance

The underlying patient-level data are not publicly available.

The study used linked, pseudonymised patient-level data within the Whole Systems Integrated Care (WSIC) secure data environment. These data are subject to NHS information governance requirements and cannot be shared publicly.

Access to the underlying data may be possible through the relevant governance and data-access processes, including approval by the appropriate Northwest London Data Access Committee and compliance with OneLondon secure data environment requirements.

The code in this repository therefore cannot be run directly on publicly available data to reproduce the study results. It is provided to improve transparency around the analytical methods and to support methodological reproducibility.

Code availability

The SQL and R scripts used for data extraction, processing and analysis are provided in this repository.

The scripts were developed specifically for use within the WSIC Secure Data Environment and may require adaptation for use with other healthcare datasets, data models or secure data environments.

Because the underlying WSIC data and associated data dictionaries are not publicly available, users should not expect the scripts to run without modification in another environment.

Study population

The study identified patients referred to a North West London Rapid Diagnostic Centre between November 2021 and December 2024.

Following linkage to WSIC primary-care records, 2,021 patients with available primary-care records were included in the analysis.

The RDC referral dataset was used as the definitive source for cohort identification because identification based solely on the dedicated SNOMED CT referral code did not capture all referrals. (Nature)

Key methodological components

The analysis code supports the following components of the study:

Cohort identification and linkage

* linkage of RDC referral records with WSIC primary-care records
* definition of the index date
* identification of the analysis cohort
* assessment of completeness of linked primary-care information

Clinical and demographic variables

Variables included:

* age and sex
* ethnicity
* deprivation
* comorbidities
* frailty
* smoking
* alcohol use
* weight loss
* non-specific symptoms

Laboratory investigations

The analysis included selected laboratory investigations such as:

* full blood count
* liver and kidney function tests
* PSA
* CA-125
* ESR
* CRP
* ferritin
* HbA1c
* calcium
* quantitative FIT

Laboratory results were assessed using the study’s predefined definitions and reference ranges. (Nature)

Healthcare utilisation

The analysis examined primary-care contacts, including:

* face-to-face consultations
* telephone consultations
* home visits
* video consultations
* other relevant primary-care encounters

Repeated contacts occurring on the same day were handled according to the methodology described in the manuscript.

Prescribing

Medication exposures were grouped into clinically relevant classes using the coding framework described in the manuscript.

Incident prescribing was defined using the earliest recorded prescription within the available primary-care history where applicable.

Outcomes

The analysis examined:

* cancer diagnosis
* cancer subtype
* non-cancer diagnoses
* timing of diagnosis
* subsequent cancer diagnoses during follow-up

Cancer ascertainment was based on coded primary-care data available within WSIC. National cancer registry linkage was not available for this study. (Nature)

Reproducibility

This repository is intended to provide a transparent record of the analytical approach used in the published study.

Full computational reproducibility is limited by the following:

1. The underlying patient-level WSIC data cannot be publicly released.
2. Access to the WSIC Secure Data Environment is governed by NHS information-governance requirements.
3. Some data structures and reference catalogues are specific to the WSIC environment.
4. Some preprocessing and data-management steps depend on the secure environment and its underlying data model.

Accordingly, the repository should be considered a research-code companion to the publication, rather than a standalone executable analysis package.

Ethical and governance considerations

The analysis used pseudonymised healthcare data within a secure NHS data environment.

No patient-level data are included in this repository.

Users should not attempt to reconstruct, infer or identify individual patients from any materials associated with this repository.

Related publication

Gupta S, Alied M, Rafiq M, et al.

Validating a linked primary–secondary care data platform for analysis of non-specific cancer symptom pathways: a retrospective study.

npj Digital Public Health. 2026;1:34.

DOI: https://doi.org/10.1038/s44482-026-00040-8

Article: https://www.nature.com/articles/s44482-026-00040-8

Citation

If you use or adapt the code or analytical approach, please cite the associated publication:

Gupta S, Alied M, Rafiq M, et al. Validating a linked primary–secondary care data platform for analysis of non-specific cancer symptom pathways: a retrospective study. npj Digital Public Health. 2026;1:34. https://doi.org/10.1038/s44482-026-00040-8

Acknowledgements

This work was supported by the NIHR Royal Marsden & Institute of Cancer Research Biomedical Research Centre (BRC) and the Royal Marsden Cancer Charity Early Diagnosis Team.

The RM partners and OneLondon NHS Digital grant supported one year of Sunnia Gupta and Ceire Costelloe salary and enabled the work with WSIC.

Meena Rafiq is supported by a Cancer Research UK ACED Pathway Award (EDDAPA-2023/100001).

We thank Eamon O’Doherty for his support in developing SQL scripts for deriving non-specific cancer symptom diagnostic pathways within the WSIC platform and for guidance on data access and curation.

We also acknowledge the wider WSIC team and the patient and public involvement contributors who supported interpretation of the findings and review of the manuscript.

License

The code in this repository is provided for research and transparency purposes.

Before adding a formal open-source licence, the repository owners should confirm the appropriate licence and any institutional requirements governing release of the code.

⸻

Repository:
https://github.com/sg-stark/validating-linked-care-platform-WSIC-nss-cancer-pathways

Publication DOI:
https://doi.org/10.1038/s44482-026-00040-8
