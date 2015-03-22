# Code Book

## Source

The data:

- Source of the original data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
- Original description: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## Explanation

The attached R script (run_analysis.R) performs the following to clean up the data:

Merges the training and test sets to create a single data sets as follows (data frames with "Number of Instances" x "Number of Attributes"):

- train/X_train.txt with test/X_test.txt: a 10299x561 data frame.
- train/subject_train.txt with tsubject_test.txt: a 10299x1 data frame with subjects.
- train/y_train.txt with test/y_test.txt: a 10299x1 data frame with activity IDs

Reads features.txt and extracts only the measurements on the mean and standard deviation for each measurement. The result is a 10299x66 dframe, because only 66 out of 561 attributes are measurements on the mean and standard deviation. All measurements appear to be floating ponumbers in the range (-1, 1).

Reads activity_labels.txt and applies descriptive activity names to name the activities in the data set:

- walk
- walkingupsta
- walkingdownsta
- sitt
- stand
- lay

The script also appropriately labels the data set with descriptive names: all feature names (attributes) and activity names are convertedlower case, underscores and brackets () are removed. Then it merges the 10299x66 data frame containing features with 10299x1 data fracontaining activity labels and subject IDs. The result is saved as merged_clean_data.txt, a 10299x68 data frame such that the first colcontains subject IDs, the second column activity names, and the last 66 columns are measurements. Subject IDs are integers between 1 andinclusive. The names of the attributes are similar to the following:

- tbodyacc-mean
- tbodyacc-mean
- tbodyacc-mean
- tbodyacc-std
- tbodyacc-std
- tbodyacc-std
- tgravityacc-mean
- tgravityacc-mea

Finally, the script creates a 2nd, independent tidy data set with the average of each measurement for each activity and each subject. The resis saved as tidy_data_with_averages.txt, a 180x68 data frame, where as before, the first column contains subject IDs, the second colcontains activity names (see below), and then the averages for each of the 66 attributes are in columns 3...68. There are 30 subjects anactivities, thus 180 rows in this data set with averages.