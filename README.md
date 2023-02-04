# data-science-fundamentals

## Dataset
The dataset used for this work is a the 3-phase oil dataset.This dataset is from a physics-based simulation of a non-invasive monitoring system, used to determine the quantity of oil in a multi-phase pipeline containing a mixture of oil, water, and gas. The whole dataset includes 3 classes, which are homogeneous, annular and laminar (stratified) namely. The configurations of the flow in the pipe are shown in the following figure.

![image](https://user-images.githubusercontent.com/102625347/216758823-1720be50-0a6b-4eab-aa0a-b4b405498848.png)

The dataset contains 2 data files train data and test data. Train and test data are named as trndata.csv and tstdata.csv respectively.<br>

The last column of each file is the class label indicating the configuration of the flow in the pipe:
a value of 1 denotes homogeneous, a value of 2 denotes annular, and a value of 3 denotes laminar.

### Task 1: Data pre-processing and data exploration<br>
a. Use Pandas to load the data and report the number of data points (rows) in the training set and the test set, respectively.<br>
b. Report the number of features in the dataset and the number of data points in each class for the training set and the test set, separately.<br>
c. Do random permutations for the training data using the function, shuffle, from sklearn.utils. You must set a value for the parameter, random_state. Save the data as Training_set_I.<br>
The details on how to use shuffle can be viewed from the following link:<br>
https://scikit-learn.org/stable/modules/generated/sklearn.utils.shuffle.html<br>
d. Show one scatter plot for the training set, that is, one feature against another feature. It is your choice which two features you want to use in the scatter plot.<br><br>

### Task 2: Perform principal component analysis (PCA) on the training set Using Scikit-Learn<br>
a. Perform a PCA analysis on Training_set_I.<br>
b. Plot the data in the first principal component (PC1) and the second principal component (PC2) space and label/colour the data in the picture according to their class labels. The details on how to use matplotlib.pyplot.scatter can be viewed from the following link:
https://matplotlib.org/3.1.1/api/_as_gen/matplotlib.pyplot.scatter.html<br>
c. Report the variance captured by each principal component and generate a scree plot.<br>
d. Plot two subplots in one figure:<br>
• one for projecting the training set in the PC1 and PC2 project space, where the training data should be labelled using different colours in the picture according its class;<br>
• the other one is for the test set in the same PC space, where the test data should be labelled using different colours according to its class.<br><br>

### Task 3: Divide the whole training set into a smaller training set (II) and a validation set.<br>
a. Take out the last 300 rows from Training_set_I and save them as the validation set.<br>
b. Save the rest of rows in Training_set_I as the smaller training set (Training set II).<br><br>

### Task 4: Investigate how the number of features in the training dataset affects the model performance on the validation set<br>
In this task, let us consider the last column of each data file as a real-valued target rather than a class label. You need to use a linear regression model to finish the following. Predictions should be rounded to the nearest integer. (Note that this is a crude method for classification. After you have learnt classification algorithms, you should ideally use the classification algorithms to deal with this data. However, for the purposes of this piece of coursework, please follow the instructions given below.)<br>
a. Use Training set II to train D simple linear regression models, with D different feature sets. That is: the first one should use the 1st feature only; the second one should use the 1st and the 2nd features; the third one should use the 1st, 2nd, and 3rd features; the fourth one should use the first 4 features, and so on.<br>
• Remember to scale the corresponding training set and the validation set.<br>
b. Produce a learning curve of the number of features used against the performance measurements. The performance should be measured on both Training set II and the validation set.<br>
c. State the optimal number of features that should be used in this work and explain why you choose it. This should all be written in your Jupyter notebook.<br>
d. Use the selected number of features to train the model using Training_set_I and report the performance on the test set.
• Remember to scale the corresponding training and test sets.<br>

### Task 5: Summarise your findings and write the conclusions using critical thinking.<br>
a. Summarize the findings for each task.<br>
b. For Task 4, is there any problem with this experimental design? If there is, what is it? How could you further improve it so that the experimental results are more reliable?<br>

