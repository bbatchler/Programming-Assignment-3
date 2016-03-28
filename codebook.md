The script run_analysis.R performs the 5 steps described in the course project's definition.

1. Merge the training and the test sets to create one data set.
The similar data(Data with same number of columns and rows) is merged using the rbind() function. 

2. Extract only the measurements on the mean and standard deviationfor each measurement.
 Only those columns with the mean and standard deviation measures are taken from the whole dataset. 
 After extracting these columns, they are given the correct names taken from features.txt.

3. Use descriptive activity names to name the activities in the data set.
  Take the activity names and IDs from activity_labels.txt and they are substituted in the dataset.
  
4. Appropriately label the data set with descriptive variables names.
  Those columns with vague column names are corrected.

5. From the data set in step 4, create a second, independent tidy data set with the average of each variable 
 for each activity and each subject.
x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.
x_data, y_data and subject_data merge the previous datasets to further analysis.
features contains the correct names for the x_data dataset, which are applied to the column names stored in mean_and_std_features, 
a numeric vector used to extract the desired data.
A similar approach is taken with activity names through the activities variable.
All_data merges x_data, y_data and subject_data in a big dataset.

