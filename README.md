# Prediction of US Visa Application Decision using a Decision Tree and Random Forests

Prediction was into two classes - Visa Certified and Visa Denied

The number of fatures, initially 152, were reduced to the top 15 features.

Python - 2.7

### Modules used:
1. numpy
2. pandas
3. matplotlib
4. seaborn
5. sklearn
6. random
7. pickle

Dataset:
https://www.kaggle.com/jboysen/us-perm-visas/data

Download the dataset as us_perm_visas.csv and save it in the same folder as the rest of the code. The data is highly unbalanced and most of the features are empty.

The file *Visa_Visualization_Feature_Selection_Cleaning.ipynb* contains code which visualises the data. Features are selected based on if they are populated enough, if they are relevant to the problem, and if they convey meaningful information. This file also contains code to clean the data and make it useable for training. 

*Visa_Training.ipynb* has the random forest with k-fold Grid Search using scikit-learn. One of the folds is randomly selected, and the model trained using the best hyper-parameters is chosen as the final model and saved as the file best_model.

*Visa_Predictions.ipynb* has code to predict the visa statuses of an array of features.

### Files used and created
1. us_perm_visas.csv: Downloaded file from the link provided.
2. saved_mapping: This contains a list of mappings used on features. This should be used to convert a new datapoint into the form required for prediction. For example company names can be mapped to numbers.
3. data: The dataframe containing the selected features after cleaning and processing is stored in data, and is created at the end of Visa_Visualization_Feature_Selection_Cleaning.ipynb. This file is loaded and used in Visa_TRaining.ipynb. 
4. models: Contains the results of the k-fold Grid Search. Is a list of tuples containing the Grid Search OBject, Test and Train Data, and Train and Test Accuracies of each fold.
5. best_model: One of the folds is randomly selected and the Grid Search object of that fold is saved in best_model. This can be used for future predictions.

These files exceed the maximum file size on Github and have not been uploaded. These can be created by running the code.

A detailed report of the results is found in Results.pdf
