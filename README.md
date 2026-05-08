# Background

Stroke are among the leading causes of death and long-term disability worldwide. Early detection and timely treatment are of great importance for reducing patient mortality and disability rates. Compared with invasive monitoring methods, non-invasive cerebral monitoring technologies offer several advantages, including lower risk, repeatability, and suitability for long-term bedside monitoring, making them widely used in both clinical practice and scientific research. Currently, commonly used non-invasive cerebral monitoring techniques include electroencephalography (EEG), transcranial Doppler ultrasonography (TCD), and functional near-infrared spectroscopy (fNIRS). Among them, EEG reflects neural electrical activity, TCD evaluates cerebral hemodynamic status, and fNIRS provides information on cerebral tissue oxygenation. These monitoring signals can be used not only for disease detection but also as objective indicators for prognosis prediction of brain diseases.

At present, numerous publicly available datasets support disease detection and prognosis studies based on single-modality cerebral monitoring data. For example, EEG has been widely used for the automated detection of epilepsy, Alzheimer’s disease, and stroke; TCD has been applied to the study of cerebrovascular stenosis and related disorders; and fNIRS has been utilized for the auxiliary assessment of abnormal brain function. In addition, some studies have attempted to combine two modalities among EEG, TCD, and fNIRS for prognosis prediction. Existing studies have demonstrated that the joint analysis of multi-source non-invasive cerebral monitoring data generally outperforms single-modality analysis. However, current publicly available datasets still lack multimodal data that simultaneously include EEG, TCD, and fNIRS signals, as well as prognosis labels corresponding to standardized clinical assessment scales. This limitation hinders the evaluation and comparison of prognosis prediction models.

# Dataset Introduction

To address the limitations of existing publicly available datasets in multimodal non-invasive cerebral monitoring, we constructed and released a multi-source non-invasive cerebral monitoring dataset named MNCMS. The dataset includes 30 healthy subjects and 60 patients with brain diseases. The healthy cohort consists of 15 males and 15 females, while the patient cohort includes 40 males and 20 females. All participants were over 50 years old. The patient cohort comprises 30 patients with cerebral infarction, 15 patients with intracerebral hemorrhage, and 15 patients with subarachnoid hemorrhage.

The MNCMS dataset contains multiple synchronized EEG, TCD, and fNIRS monitoring sessions collected from postoperative days 1–5 for each patient. Each monitoring session lasted approximately 20 minutes, and the actual prognosis outcomes at 14 days after discharge were also recorded. Based on the widely used modified Rankin Scale (mRS), standardized prognosis labels were assigned to each patient and categorized into three groups: “good prognosis,” “moderate prognosis,” and “poor prognosis.” For healthy subjects, approximately 20 minutes of synchronized EEG, TCD, and fNIRS monitoring data were collected correspondingly.

All patient data were collected in the Neurological Intensive Care Unit (NICU) of Xiangya Hospital, Central South University, while healthy subjects were recruited from community hospitals. Written informed consent was obtained from all participants. The study protocol was approved by the institutional ethics committee and strictly followed the principles of the Declaration of Helsinki.

# Contributions of the Dataset

The MNCMS dataset has the following key contributions:

- It addresses the limitation of existing publicly available datasets that lack simultaneous coverage of EEG, TCD, and fNIRS non-invasive cerebral monitoring signals, thereby providing a unified data foundation for multimodal non-invasive cerebral monitoring research.

- It covers three representative stroke subtypes, including cerebral infarction, intracerebral hemorrhage, and subarachnoid hemorrhage, and provides standardized prognosis labels for all patients. This enables the dataset to support not only disease detection and prognosis prediction studies within individual stroke populations, but also comparative analyses across different stroke subtypes.

- During the dataset construction process, gender-related factors were taken into consideration, and the gender distribution of participants was carefully controlled. As a result, the dataset can further support studies focusing on gender-based differences and analyses.

  # Dataset Description

<div align="center">
  <img src="https://github.com/csuvis/MNCMS_dataset/blob/main/png/image-20260508165547987.png" width="400"/>
</div>
  
An overview of the MNCMS dataset organization is illustrated in the figure. The MNCMS dataset consists of two main components: participant metadata and non-invasive cerebral monitoring data. The participant metadata are stored in the ***Participant_metadata.xlsx*** file. Each row in this file corresponds to a participant and contains four fields: ***ID***, ***Sex***, ***Diagnosis***, and ***Prognosis***. Non-invasive cerebral monitoring data from 30 healthy subjects are stored in the ***Healthy Subjects*** directory, and data from 60 stroke patients are stored in the ***Stroke Patients*** directory. All monitoring data are provided in Comma Separated Values (CSV) format. Each monitoring session is organized as multivariate time-series data with 21 channels, which can be categorized into four types: ***time***, ***EEG signals***, ***TCD signals***, and ***fNIRS signals***.
