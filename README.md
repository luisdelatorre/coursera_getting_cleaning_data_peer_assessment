coursera_getting_cleaning_data_peer_assessment
==============================================

Peer Assessments /Getting and Cleaning Data Course Project
## The files and code for the peer assessment

##### The description of the script works ######

For 1st tiny data set:

Read data sets and combine them
Read subjects and combine them
Read data labels and combine them
Read features list
Subset only only std and mean features from list
Perform same subset on data set
Rename features to be more human readable
Read activity list
Rename activities to be more human readable
Rename data labels with activity name
Merge data, subjects, and labels to single tiny data set
Write tiny data set to file
For 2nd tiny data set: average of measurement for activity and subject

Prepare empty data set of appropriate length for
Loop through subjects, then subloop through activities
For each activity in a subject, get the full list of measurements
Calculate the mean of each of these activities
Place the means in subsequent columns of the subject/activity row
Write second tiny data set to file

############ The code book for variables #######

Source https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

The script run_analysis.R performs the following process to clean up the data and create tiny data sets:

Merge the training and test sets to create one data set.

Reads features.txt and uses only the measurements on the mean and standard deviation for each measurement.

Reads activity_labels.txt and applies human readable activity names to name the activities in the data set.

Labels the data set with descriptive names. (Names are converted to lower case; underscores and brackets are removed.)

Merges the features with activity labels and subject IDs. The result is saved as tidyData.txt.

The average of each measurement for each activity and each subject is merged to a second data set. The result is saved as tidyData2.txt.

Variables

testData - table contents of test/X_test.txt
trainData - table contents of train/X_train.txt
X - Measurement data. Combined data set of the two above variables
testSub - table contents of test/subject_test.txt
trainSub - table contents of test/subject_train.txt
S - Subjects. Combined data set of the two above variables
testLabel - table contents of test/y_test.txt
trainLabel - table contents of train/y_train.txt
Y - Data Labels. Combined data set of the two above variables.
featuresList - table contents of features.txt
features - Names of for data columns derived from featuresList
keepColumns - logical vector of which features to use in tidy data set
activities - table contents of activity_labels.txt. Human readable
tidyData - subsetted, human-readable data ready for output according to project description.
uS - unique subjects from S
nS - number of unique subjects
nA - number of activities
nC - number of columns in tidyData
td - second tiny data set with average of each variable for each activity and subject
Output

tidyData.txt

tidyData.txt is a 10299x68 data frame.

The first column contains subject IDs.
The second column contains activity names.
The last 66 columns are measurements.
Subject IDs are integers between 1 and 30.
tidyData2.txt

tidyData2.txt is a 180x68 data frame.

The first column contains subject IDs.
The second column contains activity names.
The averages for each of the 66 attributes are in columns 3-68.
