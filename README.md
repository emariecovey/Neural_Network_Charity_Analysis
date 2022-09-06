# Neural_Network_Charity_Analysis

# Overview of the analysis: Explain the purpose of this analysis.
This analysis uses data from the non-profit organization, Alphabet Soup. They raise and donate money to other organizations that protect the environment and improve people's well-being. This analysis looks at previous donations and their success. The goal of this analysis is to build a machine learning model to help vet future grant applicants to help make the most successful and impactful donations. A deep neural network was created, with fairly high predictive accuracy, that can help the organization make donation decisions in the future. 

# Results:

### Data Preprocessing
- The features for the model included the following variables: 
    - APPLICATION_TYPE — Alphabet Soup application type
    - AFFILIATION — Affiliated sector of industry
    - CLASSIFICATION — Government organization classification
    - USE_CASE — Use case for funding
    - ORGANIZATION — Organization type
    - STATUS — Active status
    - INCOME_AMT — Income classification
    - SPECIAL_CONSIDERATIONS — Special consideration for application
    - ASK_AMT — Funding amount requested

- The target variable was:
    - IS_SUCCESSFUL— Was the money used effectively   

- Variables that were neither targets nor features, and were removed from the input data included:
    - EIN and NAME — Identification columns
    - APPLICATION_TYPE — Alphabet Soup application type

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
- Were you able to achieve the target model performance?
- What steps did you take to try and increase model performance?

### Summary: 
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

