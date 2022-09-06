# Neural_Network_Charity_Analysis

# Overview of the analysis: 
This analysis uses data from the non-profit organization, Alphabet Soup. They raise and donate money to other organizations that protect the environment and improve people's well-being. This analysis looks at previous donations and their success. The goal of this analysis was to build a machine learning model to help vet future grant applicants to help make the most successful and impactful donations. A deep neural network was created, with fairly high predictive accuracy, that can help the organization make donation decisions in the future. The analysis started with an original model, which was the jumping point for a more accurate optimized model. 

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
- Numbers of neurons, layers, and activation functions selected for the neural network model:
    - Neurons: 
        - Original model: I had a dataframe with 35 variables, so I started out with 35 neurons in a single layer. 
        - Optimized model: When I optimized the model, I lessened the number of variables being bucketed to try to give the model more data to work with, and my starting dataframe had 46 variables. A rule of thumb for deciding on neuron numbers is 2-3 times the number of inputs, so I started my first layer with 92 variables. Other models I've seen have generally halved the number of neurons in subsequent layers, so my second layer had 46 neurons and the third layer had 23. 
    - Layers:
        - The original model had one layer. I added two additional layers in the optimized model to help increase the accuracy of the model. 
    - Activation Functions: 
        - For both models, the first layer (and the hidden layers following that in the optimized model) used the relu activation function. I tried the sigmoid and Tanh functions in place of the relu, and they did not help the model's accuracy. The output layer on both models used the sigmoid activation function, because the outcome of this model is binary (successful or not successful). 

- Achieving the target model performance:
    - I was not able to achieve the target model performance of 75%. The last epochs in the original model had around 71.3% accuracy, and the last epochs in the optimized model were around 74.2% accuracy. The goal was 75%, and the optimized model was closer to that goal, but not quite there. When the test data was put into the models, the original model had 71.0% accuracy, while the optimized model had 72.3% accuracy. 

Last few epochs of original model:
![original](https://github.com/emariecovey/Neural_Network_Charity_Analysis/blob/main/images/original_model.png)

Last few epochs of optimized model:
![optimized](https://github.com/emariecovey/Neural_Network_Charity_Analysis/blob/main/images/refactored_model.png)

- Steps taken to try and increase model performance:
    - Binning: I lowered the threshold of the variables that were binned, so that there were less groups included in the "other" bins. My thinking was that this would give the model more data to work with, and it resulted in the model having more variables. 
    - Hidden layers: I added two hidden layers to help the model have more chances to detect patterns
    - Neurons: I added more neurons to the first layer to help the model have more chances to detect patterns
    - Activation functions: I tried changing the activation functions in the hidden layers, but I did not keep that change since I didn't see a great difference in the accuracy
    - Noisy Variables: I dropped the "Status" variable, that records the current status of the application. That variable didn't seem to have any influence on whether or not the donation would be successful or not, so I removed it. 

### Summary: 
In summary, both models accurately predicted if an application would be successful or not, around 72% of the time. 

After playing around with this model for quite a while, I wrote the code for a SVM (support vector machine) model, which also had a 72% accuracy and was written in three lines of code. A SVM model may be preferable to a neural network model, because it is less likely to be overfitted, provides the same accuracy, and is much simpler code to write. 


