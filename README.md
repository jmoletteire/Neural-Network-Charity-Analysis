# Neural Network Charity Analysis
## Overview
Creating a binary classifier that is capable of predicting whether 
applicants will be successful if funded by Alphabet Soup.
<br>

## Results
### _Data Preprocessing_
* _**What variable(s) are considered the target(s) for your model?**_
  * **IS_SUCCESSFUL** — was the money used effectively?
<br></br>

* _**What variable(s) are considered to be the features for your model?**_
  * **APPLICATION_TYPE** — Alphabet Soup application type
  * **AFFILIATION** — Affiliated sector of industry
  * **CLASSIFICATION** — Government organization classification
  * **USE_CASE** — Use case for funding
  * **ORGANIZATION** — Organization type
  * **STATUS** — Active status
  * **INCOME_AMT** — Income classification
  * **SPECIAL_CONSIDERATIONS** — Special consideration for application
  * **ASK_AMT** — Funding amount requested
<br></br>

* _**What variable(s) are neither targets nor features, and should be removed from the input data?**_
  * **EIN** and **NAME** — Identification columns

<br></br>

### _Compiling, Training, and Evaluating the Model_
* _**How many neurons, layers, and activation functions did you select for your neural network model, and why?**_
  * The first model used a single hidden layer with one neuron and a ReLU activation function. 
    It was a simple test to set a baseline accuracy.
  * Other models used two hidden layers with far greater neurons
    (between 5 and 80 per layer), and tested Leaky ReLU and tanh activation functions.
    This was in an effort to test a wide range of neuron, layer, and activation
    function combinations.
<br></br>

* _**Were you able to achieve the target model performance?**_
  * Target performance was not achieved by any model.
  * The simple model (1 hidden layer, 1 neuron) produced a relatively ineffective model for predicting investment success,
    correctly labeling loans at a 72% clip.
  * Later models increased the number of neurons and hidden layers, and altered the
    activation function, all with similar results, and none surpassing 73% accuracy.
<br></br>

* _**What steps did you take to try and increase model performance?**_
  * To increase model performance, additional neurons and hidden layers were added, and several
    activation functions were tested, but none produced a model that was significantly more
    accurate than the simple model.
<br></br>

## Summary
In conclusion, the models tested were not as accurate as expected. Given the range of 
neuron counts and activation functions already tested, it seems a solution would involve
a model that considers fewer features and has an extra hidden layer.<br>

To elaborate, removing features could quiet any noisy and irrelevant variables that hinder training, and it
may also help to re-examine the dataset and determine if there are any outliers or obvious
candidates for removal. Additionally, extra hidden layers would allow the model to more closely evaluate
data, which should lead to more accurate predictions, although I would recommend adding only one additional
layer first, then adding more if it is deemed necessary.
<br></br>