============================================================
SIT307 — TASK 11.1HD
MACHINE LEARNING MINI RESEARCH
============================================================

Student: Raghav Sharma
Unit: SIT307


------------------------------------------------------------
ABOUT THIS PROJECT
------------------------------------------------------------

For this project, I have performed the same heart disease
classification experiments as done in the paper written by Bhagat
et al. I trained all six models separately and the Stacking Ensemble,
and then compared my results with the results of the paper.

In the process of reproducing the experiments, I noticed that there
are many duplicate records in the data set. In Part 2, I have
dropped those records and experimented with the 302 unique records.
I have performed one train/test split first and then repeated
cross-validation on the results.


------------------------------------------------------------
FILES INCLUDED
------------------------------------------------------------

1. HD PROJECT OF MACHINE NOTEBOOK.ipynb

   This is the Jupyter notebook containing the code, saved outputs,
   results and discussion for Parts 1 and 2.

2. heart.csv

   This is the dataset read by the notebook. It has 1,025 rows and
   14 columns, including the target column.

3. README.txt

   This file explains how to install the required packages and run
   the notebook.


------------------------------------------------------------
SOFTWARE AND INSTALLATION
------------------------------------------------------------

I used Python 3.12.3 for the experiments. Python 3.12 is recommended
when running the notebook again.

After extracting the ZIP, open Command Prompt in the folder containing
the notebook and heart.csv. Install the required packages with:

python -m pip install numpy==1.26.4 pandas==2.2.3 scikit-learn==1.5.1 xgboost==3.4.1 matplotlib seaborn notebook

The package versions shown above match the versions recorded for
NumPy, pandas, scikit-learn and XGBoost in my notebook. Matplotlib,
seaborn and Jupyter Notebook are also required to run all cells.


------------------------------------------------------------
HOW TO RUN
------------------------------------------------------------

1. Extract the ZIP file.

2. Check that HD PROJECT OF MACHINE NOTEBOOK.ipynb, heart.csv and
   README.txt are together in the extracted folder.

3. Open Command Prompt in that folder and enter:

   python -m notebook

4. In Jupyter, open HD PROJECT OF MACHINE NOTEBOOK.ipynb.

5. Select Kernel > Restart & Run All. Let the notebook finish before
   checking the results. The repeated cross-validation experiment
   may take several minutes.

The notebook loads the dataset with pd.read_csv("heart.csv"). Keep the
dataset name as heart.csv and run the cells from top to bottom.


------------------------------------------------------------
WHAT THE NOTEBOOK CONTAINS
------------------------------------------------------------

In Part 1, Logistic Regression, Decision Tree, Random Forest,
XGBoost, Naïve Bayes, KNN, and Stacking Ensemble models are trained.
Accuracy, Precision, Recall, F1, and AUC are compared to those
indicated in the chosen article.

Additionally, preprocessing effects are tested for the Logistic
Regression model. Comparing Min-Max, Standard Scaling, and Median
Imputation + Standard Scaling preprocessing methods on the same
train/test split is performed.

Part 2 performs removal of exact duplicates prior to evaluating.
The first experiment in Part 2 applies the stratified split with
the size of 61 test records. The second experiment implements the
stratified five-fold cross-validation repeated three times on all 302
records. The notebook provides the mean and standard deviation of
five measures of performance for each of the 15 validation folds.

The test result with 61 records is one particular result. It is
not supposed to be considered as an average value of cross-validation
results. For reproducibility, random state 42 is set up wherever
possible.


------------------------------------------------------------
SOURCE OF THE DATA
------------------------------------------------------------

The heart disease dataset came from Kaggle. The selected research
paper and dataset are identified in the notebook's References section.


============================================================
END OF README
============================================================