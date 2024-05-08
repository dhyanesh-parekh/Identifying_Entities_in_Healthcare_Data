# Identifying Entites in Healthcare Data
> ‘BeHealthy’ has a web platform that allows doctors to list their services and manage patient interactions and provides services for patients such as booking interactions with doctors and ordering medicines online. Here, doctors can easily organise appointments, track past medical records and provide e-prescriptions.
So, companies like ‘BeHealthy’ are providing medical services, prescriptions and online consultations and generating huge data day by day.
Let’s take a look at the following snippet of medical data that may be generated when a doctor is writing notes to his/her patient or as a review of a therapy that he or she has done.
“The patient was a 62-year-old man with squamous cell lung cancer, which was first successfully treated by a combination of radiation therapy and chemotherapy.”
As you can see in this text, a person with a non-medical background cannot understand the various medical terms. We have taken a simple sentence from a medical data set to understand the problem and where you can understand the terms ‘cancer’ and ‘chemotherapy’. 
Suppose you have been given such a data set in which a lot of text is written related to the medical domain. As you can see in the dataset, there are a lot of diseases that can be mentioned in the entire dataset and their related treatments are also mentioned implicitly in the text, which you saw in the aforementioned example that the disease mentioned is cancer and its treatment can be identified as chemotherapy using the sentence.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Research Flow](#research-flow)
* [Acknowledgements](#acknowledgements)
* [Contributor](#contributor)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- Business Problem
  - **BeHealthy** has a web platform that allows doctors to list their services and manage patient interactions and provides services for patients such as booking interactions with doctors and ordering medicines online. Here, doctors can easily organise appointments, track past medical records and provide e-prescriptions. Suppose you have been given such a data set in which a lot of text is written related to the medical domain, you can build an algorithm to map the diseases and their respective treatment, to determine the disease name and its probable treatment from the dataset and list it out in the form of a table or a dictionary
  - **Concept identification:** 
        After preprocessing, we will first explore what are the various concepts present in the dataset. For this task, we will use PoS tagging. It is good to identify all the words from the corpus that have a tag of NOUN or PROPN (nouns) and prepare a dictionary of their counts. We will then output the top 25 most frequently discussed concepts in the entire corpus.An important point to note here is that we are using both test and train sentences for concept identification. This is an exploratory analysis on the complete data. In this step, you need to perform the following two tasks by considering the train and the test dataset as a single unit of data:Use a toolkit like spaCy to extract those tokens that have NOUN or PROPN as their PoS tag and find their frequency from the entire dataset that comprises both the train and the test datasets.Print the top 25 most common tokens with NOUN or PROPN PoS tags for the entire dataset that comprises both the train and the test datasets.
  - **Defining the features for CRF:** 
    Here, you need to perform the following three steps:
    - Define the features with the PoS tag as one of the features.
    - While defining the features in which you have used the PoS tags, you also need to consider the preceding word of the current word. The    use of the information of the preceding word makes the CRF model more accurate and exhaustive.
    - Mark the beginning and the end words of a sentence correctly in the form of features.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Research Flow
- Data preprocessing
- EDA
- Concept identification
- Defining the features for CRF
- Getting the features words and sentences
- Defining input and target variables
- Building the model
- Evaluating the model
- Identifying the diseases and predicted treatment using a custom NER


<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- Numpy - version 1.23.5
- Pandas - version 1.5.3
- Matplotlib - version 3.7.1
- Seaborne - version 0.12.2
- Scikit-learn - version 1.2.2
- Statsmodels - version 0.14.0


<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
Giving credits here.
- This project was inspired by [UpGrad](https://ww2.upgrad.com/?_gl=1*1a6yjvu*_ga*MTY4NTk0NDA2Ny4xNjk4MDg2ODEw*_ga_HVXPGHVCS0*MTY5ODA4NjgwOS4xLjAuMTY5ODA4NjgwOS42MC4wLjA.&user_uuid=478408e8-483a-4336-8184-9025c279e0af&combination_id=2) and [IIIT Banglore](https://www.iiitb.ac.in/)


## Contributor
Created by [@Dhyanesh_Parekh](https://github.com/dhyanesh-parekh) - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
