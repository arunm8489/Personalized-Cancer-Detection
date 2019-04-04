# Personalized-Cancer-Detection

Classify the given genetic variations/mutations based on evidence from text-based clinical literature

## Business problem to solve
Understanding the business problem to solve is very important, that lets us know the real world constraints.so lets discuss more about it, without business constraints we cant put our models into production.

When a patient seems to have cancer, we take a cancer tumor from the patient and we go through genetic sequencing of DNA.Once sequenced, cancer tumor can have thousands of genetic mutations.‘mutation’ means a small change in gene which causes cancer. Here every gene is assosiated with a variation.Now with the help od gene and variation we need to classify which class it belongs to. We have 9 classes in our dataset out of which only few belongs to cancer classes.

According to this source (https://www.kaggle.com/c/msk-redefining-cancer-treatment/discussion/35336#198462), these are steps to be done manually to classify,

A molecular pathologist selects a list of genetic variations of interest that he/she want to analyze
The molecular pathologist searches for evidence in the medical literature that somehow are relevant to the genetic variations of interest
Finally this molecular pathologist spends a huge amount of time analyzing the evidence related to each of the variations to classify them. Here, steps 1 and 2 can be done, but doing step 3 takes a lot of time, so we reduce time consuming using a machine learning model.
Finally our problem statement is __ classify genetic variations based on evidence from the text based clinical literature or research papers, which is multi-class classification problem __ because we have 9 classes.

## Business constraints
Interpretability of the algorithm is must because, at the end doctor or specialist should understand why this model predicted that class.
No low-latency requirement which means patient can wait few minutes for results. This tells us that we can use complex models.
Errors are very costly.
Probabilities of data point to each class needed because, if two classes have somewhat simillar probs,doctor may suggest patient to go with more tests.

## Performance metrics
Multi class Log-Loss,confusion matrix(Log-Loss is chosen because it actually uses probability which is our business constraint)

## Machine Learning objective: 
Predict the probability of each data point belonging to each of nine classes.

## Dataset
Data was provided by Data from Memorial Sloan Kettering Cancer Center (MSKCC) and it can be found on kaggle https://www.kaggle.com/c/msk-redefining-cancer-treatment/data. We have two data files, one conatins the information about the genetic mutations and the other contains the clinical evidence (text) that human experts/pathologists use to classify the genetic mutations.Both these data files are have a common column called ID which is used to join these two files.

