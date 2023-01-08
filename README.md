# CHOP_Data_Challenge

Data Exercise

This exercise will evaluate your ability to build a cohort of patients and calculate some metrics related to that cohort. You should have the following:

5 datasets (all data you need is found within the provided datasets)
A data dictionary defining each dataset and its fields

Instructions
We encourage you to put the data ingest and export as part of a re-usable analysis script. Examples of different functions that can be used are found here. This makes it easier for us to re-run your code in our evaluations, and it's good coding practice!

Part 1: Assemble the project cohort
The project goal is to identify patients seen for drug overdose, determine if they had an active opioid at the start of the encounter, and if they had any readmissions for drug overdose.

Your task is to assemble the study cohort by identifying encounters that meet the following criteria:

The patient’s visit is an encounter for drug overdose
The hospital encounter occurs after July 15, 1999
The patient’s age at time of encounter is between 18 and 35 (Patient is considered to be 35 until turning 36)
Part 2: Create additional fields
With your drug overdose encounter, create the following indicators:

DEATH_AT_VISIT_IND: 1 if patient died during the drug overdose encounter, 0 if the patient died at a different time

COUNT_CURRENT_MEDS: Count of active medications at the start of the drug overdose encounter

CURRENT_OPIOID_IND: 1 if the patient had at least one active medication at the start of the overdose encounter that is on the Opioids List (provided below), 0 if not

READMISSION_90_DAY_IND: 1 if the visit resulted in a subsequent drug overdose readmission within 90 days, 0 if not

READMISSION_30_DAY_IND: 1 if the visit resulted in a subsequent drug overdose readmission within 30 days, 0 if not overdose encounter, 0 if not

FIRST_READMISSION_DATE: The date of the index visit's first readmission for drug overdose. Field should be left as N/A if no readmission for drug overdose within 90 days

Part 3: Export the data to a CSV file

Export a dataset containing these required fields:

Field name	Field Description	Data Type

PATIENT_ID	Patient identifier	Character String

ENCOUNTER_ID	Visit identifier	Character string

HOSPITAL_ENCOUNTER_DATE	Beginning of hospital encounter date	Date/time

AGE_AT_VISIT	Patient age at admission	Num

DEATH_AT_VISIT_IND	Indicator if the patient died during the drug overdose encounter. Leave N/A if patient has not died,	0 /1

COUNT_CURRENT_MEDS	Count of active medications at the start of the drug overdose encounter	Num

CURRENT_OPIOID_IND	if the patient had at least one active medication at the start of the overdose encounter that is on the Opioids List (provided below)	0/1

READMISSION_90_DAY_IND	Indicator if the visit resulted in a subsequent readmission within 90 days	0/1

READMISSION_30_DAY_IND	Indicator if the visit resulted in a subsequent readmission within 30 days	0/1

FIRST_READMISSION_DATE	Date of the first readmission for drug overdose within 90 days. Leave N/A if no readmissions for drug overdose within 90 days.	Date/time

Opioids List:

Hydromorphone 325Mg

Fentanyl – 100 MCG

Oxycodone-acetaminophen 100 Ml
