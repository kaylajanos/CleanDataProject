##Overview 
The run_anlaysis code can be used to read in and clean up samsung wearbable device data found here: <br>
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip <br>
<br>

Information on these datasets can be found here: <br>
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones  <br>


#What this code does <br>
1. Downloads and upzips file from webiste above 
2. Reads in the feature names, which will be added to the test and training datasets once read in
	- Analyzes the feature names for only those that contian mean and std values, which is what we want 
3. Reads in the activity names/label values
4. Reads in the test data	
	- starts with test_x which is just the numeric values for each feature names
	- assigns the feature names from the feature names file read in previously 
	- subsets the features for only the values we want (determined in step 2)
	- reads in test_y which contains the numeric value that identifies each rows activity 
	- reads in subjects for test, each row in subjects corresponds to each row in test_x 
	- combines subjects, activity, and feature names into one table (test)
	- merges activity name from step 2 onto test dataset 
	- removes unneeded data 
5. Repeats step 4 for test data 
6. Cleans up variable names 
7. Takes mean of each variable grouped by subject and activity 
	- Creates tidy dataset from data ^ 
	- Outputs dataset 




