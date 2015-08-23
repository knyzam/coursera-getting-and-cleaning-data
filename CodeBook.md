Introduction

run_analysis codes performs 5 steps based on below's project's definition

    1. Data in files having the same number of columns and referring to the same entities are merged using the rbind() function.
    2. Columns with the mean and standard deviation measures are taken from the whole dataset. They are given the correct names after extracting the whole columns taken from features.txt.
    3. The activity names and IDs from activity_labels.txt are taken and are substituted in the dataset.
    4. On the whole dataset, those columns with vague column names are corrected.
    5. A new dataset are generated with all the average measures for each subject and activity type. The output file is called average.txt.

Variables

    1. x_train, y_train, x_test, y_test, subject_train and subject_test = contain data from files given by coursera.
    2. x_data, y_data and subject_data = merged previous datasets.
    3. features contains the correct names for the x_data dataset, which are applied to the column names stored in mean_and_std_features, a numeric vector used to extract the desired data.
    4. A similar approach is taken with activity names through the activities variable.
    5. all_data merges x_data, y_data and subject_data in a big dataset.
    6. averages_data contains averages which will be stored in a text file. 
    7. ddply()is used to apply colMeans().
