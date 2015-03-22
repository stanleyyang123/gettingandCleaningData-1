The run_analysis.R code does the following steps
1. Read X_train.txt, y_train.txt and subject_train.txt from the "./data/train" folder and store them in trainData, trainLabel and trainSubject variables respectively.
2. Read X_test.txt, y_test.txt and subject_test.txt from the "./data/test" folder and store them in testData, testLabel and testsubject variables respectively.
3. Combine testData to trainData to generate a new data frame, joinData; combine testLabel to trainLabel to generate another data frame which is joinLabel; combine testSubject to trainSubject and generate new data frame which is joinSubject.
4. Read the features.txt file from the "/data" folder and store the data in a variable called features. We only extract the measurements on the mean and standard deviation. This results in a 66 indices list. We get a subset of joinData with the 66 corresponding columns.
5. Clean the column names of the subset. We remove the "()" and "-" symbols in the names, as well as make the first letter of "mean" and "std" a capital letter "M" and "S" respectively.
6. Read the activity_labels.txt file from the "./data"" folder and store the data in a variable called activity.
7. Clean the activity names in the second column of activity. We first make all names to lower cases. If the name has an underscore between letters, we remove the underscore and capitalize the letter immediately after the underscore.
8. Transform the values of joinLabel according to the activity data frame.
9. Combine the joinSubject, joinLabel and joinData by column to get a new cleaned data frame named cleanedData. Properly name the first two columns, "subject" and "activity". 
10. Write the cleanedData out to "merged_data.txt" file in current working directory.
11. Finally, generate a second independent tidy data set with the average of each measurement for each activity and each subject. 
12. Write the final output to "data_with_means.txt" file in current working directory