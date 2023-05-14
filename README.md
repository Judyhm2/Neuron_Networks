# ML: Neuron Networks
## Overview
For this project, I will create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. I whave used a charity data csv file that contains more than 34,000 organizations that have received funding from Alphabet Soup business over the years. There are three technical analysis deliverables as follows:

- Deliverable 1: Preprocessing Data for a Neural Network Model (see file [AlphabetSoupCharity](https://github.com/Judyhm2/Neuron_Networks/blob/main/AlphabetSoupCharity.ipynb))
- Deliverable 2: Compile, Train, and Evaluate the Model (see file [AlphabetSoupCharity](https://github.com/Judyhm2/Neuron_Networks/blob/main/AlphabetSoupCharity.ipynb))
- Deliverable 3: Optimize the Model (see file [AlphabetSoupCharity_Optimization](https://github.com/Judyhm2/Neuron_Networks/blob/main/alphabetsoup_optimization.h5))
## Results
### Deliverable 1: Preprocessing Data for a Neural Network Model
- To Preprocess the Data, I imported csv file charity_data. I then, used "EIN" and "NAME" to drop non-beneficial columns. To Determine the unique values of each column, I generated application_cat as a categorical variable. To visualize the dataset, I used the column APPLICATION_TYPE to plot the data for the graph based on density. 
- See graph below 

![](https://github.com/Judyhm2/Neuron_Networks/blob/main/1.png)
- To Create a OneHotEncoder instance, I fitted and transformed the OneHotEncoder in the variable encode_df, which I then placed into a dataframe of said name. Afterwards, I merged one-hot encoded features and dropped the originals. 
- See image below 

![](https://github.com/Judyhm2/Neuron_Networks/blob/main/1_2.png) 

### Deliverable 2: Compile, Train, and Evaluate the Model
- To compile the model, I first defined, deep neural net, by using the number of input features and hidden nodes for each layer. 
- See image below. 
![](https://github.com/Judyhm2/Neuron_Networks/blob/main/1_3.png)

- The model was compiled and trained to fit 100 epochs.
- The evaluation of the model using the test data resulted in the following
- 268/268 - 0s - loss: 0.0489 - accuracy: 0.9900 - 396ms/epoch - 1ms/step Loss: 0.04886231571435928, Accuracy: 0.989970862865448 

### Deliverable 3: Optimize the Model
- To Optimize the Model, I imported checkpoint dependencies. I then, created a compilation model using (loss="binary_crossentropy", optimizer="adam", metrics=["accuracy"]). I created a callback that saves the model's weights in 100 epochs, through training and evaluation of the data.
- The model resulted in the following268/268 - 0s - loss: 0.0081 - accuracy: 0.9991 - 371ms/epoch - 1ms/step Loss: 0.008060415275394917, Accuracy: 0.9990670680999756.
- I then exported and imported the model to the HDF5 file, "alphabetsoup_optimization.h5".
- See image below 
-![](https://github.com/Judyhm2/Neuron_Networks/blob/main/1.png)
## Summary
In the first deliverable, the merger of the files resulted in a merged dataset of 5 rows and 44 columns. For Deliverable, the model "sequential" had Total params: 395, Trainable params: 395 and Non-trainable params: 0. In Deliverable 3, for optimization the results shows that loss and accuracy of the model indicates 268/268 - 0s - loss: 0.0081 - accuracy: 0.9991 - 302ms/epoch - 1ms/step Loss: 0.008060415275394917, Accuracy: 0.9990670680999756.



