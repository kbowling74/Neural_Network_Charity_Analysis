# Neaural_Network_Charity_Analysis
### Overview
This analysis was completed for Alphabet Soup to help determine which of the 34,000 potential organizations will be successful if they are to recieve funding from Alphabet Soup. An initial deep learning neural network model was used on the dataset to determine if the money will be used effectively or misused by the organization so that Alphabet Soup can ensure they have the highest possible impact with their investment. 

### Results
The following results are from processing the provided data from a csv file that contained the following column ids:
- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

#### Data Preprocessing
- IS_SUCCESSFUL was determined to be the target variable for the model
- EIN and NAME columns were removed as they provided no helpful information
- APPLICATION_TYPE was binned with amounts with less than 500 being classified as 'other'
- The features were made up of the remaining 43 variables

#### Compiling, Training, and Evaluating the Model
- The first iteration of the model included 110 neurons with 80 in the first hidden layer and 30 in the second hidden layer. 
the hidden layers were activated with relu and the output layer was activated with the sigmoid function. 
- The goal was to acheive a 75% accuracy with and the first iteration of the neural network came close at 72.49% with a loss of 56.17%. <br>
<img width="661" alt="Screen Shot 2022-10-21 at 4 39 12 PM" src="https://user-images.githubusercontent.com/106560606/197292952-1f672bc3-9352-424f-9168-934ebdb7bc91.png">

#### First Optimization
- The first attempt at optimization was to remove any noisy data. The status column was removed and then the model was run with the new data. 
<img width="702" alt="1st optimization" src="https://user-images.githubusercontent.com/106560606/197293122-7c4d6ea1-9bd8-4f37-82b9-f79ccd004bc5.png">

- This resulted in an accuracy of 74.19% and a loss of 53.12%, a slight increase of accuracy and decrease in loss from the first iteration. 
- 
#### Second Optimization
- The second change made to the model was increasing the number of neurons in the hidden layers. They were changed from 80, 30 to 120 for the first layer and 60 for the second layer. 
<img width="781" alt="2nd optimm" src="https://user-images.githubusercontent.com/106560606/197293585-19713281-a2cb-4d2c-8eff-2fa6b6b7ea67.png">

- This iteration resulted in an accuracy of 74.27% and a loss of 53.24% which increased slightly in accuracy from the previous optimization but also an increase in loss. 
<img width="284" alt="Screen Shot 2022-10-21 at 4 07 52 PM" src="https://user-images.githubusercontent.com/106560606/197293784-79beade6-aa43-4891-8a14-0d74a985ac43.png">

#### Third Optimization
- The third iteration of the neural netowrk involved adding a third hidden layer with 60 nodes and changing the activation function for the second hidden layer from relu to sigmoid. 
<img width="784" alt="3rd optimization" src="https://user-images.githubusercontent.com/106560606/197293913-7013edff-4471-4c15-99e0-d2b4680b165e.png">
- This iteration resulted in a 74.21% accuracy and 53.06% loss. This was a slightly lowered accuracy score from the previous model and a slightly lower loss.

### Summary
After three attempts at optimization the third option scored the highest in accuracy at 74.31% however it was not able to reach the desired 75% accuracy. The loss is also high for all of the model iterations. Seeing that adding a third hidden layer and changing the activation functions resulted in the best outcome it could be determined that continuing to fine tune the layers one at a time an accuracy of 75% could most likely be achieved by adding one or two more layers. Also, changing to include more sigmoid activation functions in the hidden layers could possibly increase the accuracy. The sigmoid function acts closer to a classification system and may help the model. 








