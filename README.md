# Product failure prediction
A company has completed a large testing study for different product prototypes. Each prototype is used in a simulated real-world environment experiment, and absorbs a certain amount of fluid (loading) to see whether or not it fails. For each product_code there is a number of product attributes as well as a number of measurement values for each individual product, representing various lab testing methods. The aim of the project is to build a model that predicts product failures.
<br>
## Notebooks
Analysis of features distributions and correlations in the dataset can be found in the data_exploration_and_preprocessing.ipynb notebook. It also contains preprossing steps, that are needed for some models. <br> 
Decision trees, AdaBoost and ExtraTrees models were built and tuned in the trees.ipynb file. The logreg_smv.ipynb file contains logistic regression and SVM models. In order to track the progress of parameters tuning process, high level of verbosity was used in trees.ipynb and logreg_svm.ipynb files. Therefore, it is recommended to open them in Google Colab or other tools to make output of some cells easier to skip. <br>
XGBoost, LightGBM and CatBoost models were built and tuned in xgboost.ipynb, lgbm.ipynb and catboost.ipynb notebooks respectively. 
<br>
## Results
All features in the dataset turned out to be weak in terms of predicting product failure. One of the features (loading) has a low correlation with the target variable. Correlation with the target variable of other features is close to zero. <br>
<br>
AUC values of the models with tuned hyperparameters are the following:
 * logistic regression: 0.5889334619933564
 * SVC with linear kernel: 0.5887895936174851
 * CatBoost: 0.5874072932775021
 * LightGBM: 0.585539577801774
 * AdaBoost: 0.5853284951374265
 * XGBoost: 0.5852756591895497
 * Random forest: 0.5793882702509077
 * Decision tree: 0.5767857044559788
 * SVC with non-linear kernel: 0.5425866322851085
 * ExtraTrees: 0.5
