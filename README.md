# Alphabet Soup Funding Analysis
**Creator**: Angelina Murdock  
**Date**: May 2025

## Overview of the Analysis
The purpose of this analysis was to develop and evaluate a machine learning model to assist the nonprofit organization **Alphabet Soup** in selecting funding applicants who are most likely to be successful. The dataset used for this analysis contains records from over **34,000 organizations** that have received funding from Alphabet Soup in previous years.

To achieve this goal, we implemented a **deep neural network** using **TensorFlow and Keras**. This model was trained on the preprocessed data to recognize complex patterns and relationships that may predict an applicant’s likelihood of success. 

## Table of contents
- [Overview of the Analysis](#overview-of-the-analysis)
- [Results](#results)
- [Summary](#summary)
- [Installation](#installation)
- [Resources](#resources)

## Results
### Data Preprocessing
 - **Target Variable**: 
     - IS_SUCCESSFUL: Indicates whether the funding provided by Alphabet Soup was used effectively by the applicant. This binary variable (1 for success, 0 for not) is the target for the machine learning model.

  - **Feature Variables**: 

     The following columns contain organizational and application data used as features for model training:
     - APPLICATION_TYPE: Type of application submitted to Alphabet Soup
     - AFFILIATION: Sector affiliation of the organization
     - CLASSIFICATION: Government classification of the organization
     - USE_CASE: Purpose of the funding request
     - ORGANIZATION: Type or structure of the organization (e.g., Corporation, Co-op)
     - STATUS: Operational status of the organization
     - INCOME_AMT: Income category of the organization
     - SPECIAL_CONSIDERATIONS: Flags for special considerations
     - ASK_AMT: Amount of money requested by the applicant

  - **Removed Variables**: 

     The following columns were removed from the dataset because they do not contribute meaningful information to the model:
     - EIN: A unique identifier that doesn't help predict success
     - NAME: Organization name; irrelevant and non-numeric


### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
- Were you able to achieve the target model performance?
- What steps did you take in your attempts to increase model performance?


## Summary
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

### **Recommendation:**

## Installation
**1. Clone the Repository:**
```bash
git clone https://github.com/Angelinamurdock/deep-learning-challenge.git
```

**2. Open the Project**:
- Open the `AlphabetSoupCharity_Optimization.ipynb` Jupyter Notebook File to interact with the project. 

**3. View the analysis:** 
- Open the `README.md` file.

**Requirements include:**
- tensorflow
- pandas
- sklearn
- numpy
- jupyter

## Resources
- **DU Bootcamp Module 21:** Used challenge files and class materials from the bootcamp.
- **ChatGPT:** Assisted with code explanations and debugging.