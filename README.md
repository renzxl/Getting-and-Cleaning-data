==============================================================
Run_Analysis.R R-script 
on Human Activity Recognition Using Smartphones Dataset
Version 1
==============================================================
by Lorenzo Stanton
==============================================================

The run_analysis.R script reads data from the "Human Activity Recognition Using Smartphones Dataset Version 1.0" and produces a new - tidy - dataset which may be used for further analysis.

The data in the "Human Activity Recognition Using Smartphones Dataset Version 1.0" have been taken from experiments carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz data were captured. The experiments were video-recorded to label the data manually. The obtained dataset was randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 


The original dataset included the following data files: 
1) 'features.txt': List of all features.
2) 'activity_labels.txt': List of class labels and their activity name.
3) 'train/X_train.txt': Training set.
4) 'train/y_train.txt': Training labels.
5) 'train/subject_train.txt': ID's of subjects in the training data
6) 'test/X_test.txt': Test set.
7) 'test/y_test.txt': Test labels.
8)  'test/subject_test.txt': ID's of subjects in the training data



A brief description of the script:
==================================
The run_analysis.R script merges data from a number of .txt files and produces a tidy data set. 
1) It reads all required .txt files
2) It appended to the "test" and the "training" data, which are then combined into one single data frame
3) It uses the "grep" function, all the columns with mean() and std() values are extracted and then a new data frame, including only the "activity_id", the "subject_id" and the mean() and std() columns, is created    
4) It uses the "merge" function, descriptive activity names are merged with the mean/std values dataset, to get one dataset with descriptive activity names
5) It uses the "melt" and "dcast" functions of the "reshape2" package, the data is converted into a table containing mean values of all the included features, ordered by the activity name and the subject id, and the data is written to the "tidy_dataset.txt" file.


PS. this is my last class, there is too much emphasis on using R and not enough on the concepts of datascience. The use of R is too intense given I would never use R in my day to day work.
