# Alphabet Soup Funding Analysis
**Creator**: Angelina Murdock  
**Date**: May 2025

## Overview of the Analysis
The purpose of this analysis was to develop and evaluate a machine learning model to assist the nonprofit organization **Alphabet Soup** in selecting funding applicants who are most likely to be successful. The dataset used for this analysis contains records from over **34,000 organizations** that have received funding from Alphabet Soup in previous years.

To achieve this goal, we implemented a **deep neural network** using **TensorFlow** and ***Keras**. This model was trained on the preprocessed data to recognize complex patterns and relationships that may predict an applicant’s likelihood of success. 

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
**Initial Model Overview**
- **Architecture**:
   - 2 hidden layers with 80 and 30 neurons respectively.
   - ReLU activation for hidden layers and Sigmoid for the output (binary classification).
   - Designed with a basic structure to capture complex patterns and reduce them for decision-making.
- **Model Performance**:
   - Loss: 0.5578
   - Accuracy: 72.63%
- **Why It Was Updated**

   Although this model was a solid starting point, it **did not meet the target performance** of 75% accuracy, prompting a second attempt to **optimize the architecture** and improve results.

**Optimization Efforts**
1. **Feature Engineering:**
   - Binned the ASK_AMT column to convert a wide range of continuous values into categorical bins.
   - Goal: Help the model identify patterns between ranges of loan amounts and approval likelihood, reducing noise from extreme values.

2. **Model Architecture Tuning:**
   - Increased the number of units in existing layers to capture more complex patterns.
   - Added an additional Dense layer, creating a deeper network to improve learning capacity.
   - Updated structure:
      - Layer 1: 128 neurons, ReLU
      - Layer 2: 64 neurons, ReLU
      - Layer 3: 32 neurons, ReLU
      - Output: 1 neuron, Sigmoid
3. **Other Optimization Attempts:**
   - Tested multiple combinations of layers, neurons, and epoch counts.
   - Despite these efforts, performance improvements were minimal.

**Optimized Model Performance Analysis**
- **Target Performance:**
   - Unfortunately, I was not able to reach the target accuracy despite optimization.
   - Best achieved: Accuracy = 72.71%

## Summary
A deep learning model was developed to build a predictive model that could help Alphabet Soup identify funding applicants who are most likely to succeed. While the model performed reasonably well—with a best accuracy of 72.71%—it fell short of the 75% target. Multiple efforts were made to improve the model, including modifying the network structure and adjusting the data, but improvements were limited. This suggests that a deep neural network may not be the most effective solution for this particular dataset.

### **Recommendation:**
To improve results, I recommend switching to a tree-based machine learning model, such as Random Forest. These models are better suited for structured data like this, where inputs come from well-defined categories and numeric values. They tend to perform better with fewer tuning requirements, offer more interpretability, and can often achieve higher accuracy in classification problems like this one.

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