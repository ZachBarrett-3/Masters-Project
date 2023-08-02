# Predicting Endotracheal Intubation using Deep Learning

The code in this repository accompanies my research paper which is linked `Barrett_Final_Draft.pdf`. The primary objective with this repository is to provide transparency and reproducibility for the results presented in this paper. By sharing this code, I hope to encourage further research into the field of predictive medicine for ICU patients with pneumonia. 

## Code

### Pre-processing

Step 1: Obtain access to the MIMIC-III Clinical Database

You will need to complete a training regarding data security and sharing of the medical information in the database. Once you are credentialed, then you will be able to request access to the database. You can learn more about the database and the credentialing process here:

https://physionet.org/content/mimiciii/1.4/

[Google](http://www.google.com/)




The goal of pre-processing is to get an output file formatted similarly to `sample_pneumonia_reduced_vitals.csv`.


### Data processing and aggregation
The data processing and aggregation tasks are accomplished within the `Data_Prep.ipynb` Jupyter notebook. This notebook is organized to execute one specific action per code block, making it easier to troubleshoot any issues that may arise. Throughout the notebook, most steps save the current status of medical records into designated folders, providing a convenient way to verify and review the progress of the data processing tasks.


### Model implementation and evaluation

We implemented the following Deep-Learning frameworks within the `Model_Building.ipnyb` Jupyter notebook:
- Long Short-Term Memory Network (LSTM)
- Multi-layer Perceptron Network (MLP)

After training the models, we conducted a performance comparison with traditional medical modeling methodologies. The results of that comparison can be found in `Barrett_Final_Draft.pdf`. 
