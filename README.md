# Predicting Endotracheal Intubation using Deep Learning

The code in this repository accompanies my research paper `Barrett_Final_Draft.pdf`. The primary objective with this repository is to provide transparency and reproducibility for the results presented in this paper. By sharing this code, I hope to encourage and inspire further research into the field of predictive medicine. 

## Project Abstract
Pneumonia is a leading cause for admission to intensive care units (ICUs). Critically ill patients suffering from lung diseases often require endotracheal intubation to assist or regulate their breathing. Equipping healthcare professionals with accurate predictions of intubation likelihood leads to better anticipation critical events, more effective allocation medical resources, and improved patient outcomes.

This project evaluates traditional methods, such as decision trees, as well as deep learning models, including long short-term memory (LSTM) networks, in predicting the likelihood of intubation among ICU patients with pneumonia. We utilize medical data sourced from the MIMIC-III database. Specifically, we extract the vital signs recorded during the initial four hours following patients’ admission to the hospital. By focusing on this critical time frame, we aim to capture early indicators and patterns that may be informative for predicting the need for intubation among pneumonia patients in the ICU.


## Database Access
Before running the code in this repository, you will need to gain access to the [MIMIC-III Clinical Database](https://physionet.org/content/mimiciii/1.4/). Access to the database requires completing a brief training and accepting to a data privacy agreement. Once you are credentialed, you can request access to the database through your physionet account. There are multiple methods to connect to the MIMIC-III database, two of which are through AWS or BigQuery.

## Patient Vitals Extraction
For this project it is critical to extract all adults that were diagnosed with pneumonia upon admission to the ICU. In the `SQL_Queries` file, you will find some queries that helped me achieve this in a local database setting. Once you have successfully extracted all patient vital signs, you will have a file formatted similarly to the sample file `sample_pneumonia_reduced_vitals.csv`.

## Data processing and aggregation
The data processing and aggregation tasks are accomplished within the `Data_Prep.ipynb` Jupyter notebook. This notebook executes one specific action per code block and saves the current state of processed medical records, helping facilitate efficient data validation and error troubleshooting. 

## Model implementation and evaluation

We implemented the following Deep-Learning frameworks within the `Model_Building.ipnyb` Jupyter notebook:
- Long Short-Term Memory Network (LSTM)
- Multi-layer Perceptron Network (MLP)

After training the models, we conducted a performance comparison with traditional medical modeling methodologies. The results of that comparison can be found in `Barrett_Final_Draft.pdf`. 
