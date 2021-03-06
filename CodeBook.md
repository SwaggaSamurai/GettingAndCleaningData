This analysis takes data from the 
#Human Activity Recognition Using Smartphones Dataset.

The documentation that describes the data used is followed below:

##Variables:
In this analysis, all variables used were all the calculated means and standard deviations for all subjects in the study.

The output tidyDataset.txt has the variables for the means and standard deviations that were recorded during the study. This dataset is the means of the groupings of every activity and subject seperatly.

##Description of Variables:
tBodyAcc-XYZ - averaging the signals in a signal window sample, Columns for  Mean and STD respectivly
tGravityAcc-XYZ - calculation corrected for gravity used the accelerometer to collect this value
tBodyAccJerk-XYZ - the body linear acceleration and angular velocity were derived in time to obtain Jerk signals, Columns for  Mean and STD respectivly
tBodyGyro-XYZ
tBodyGyroJerk-XYZ - used the gyroscope the body linear acceleration and angular velocity were derived in time to obtain Jerk signals, Columns for  Mean and STD respectivly
tBodyAccJerkMag - the body linear acceleration and angular velocity were derived in time to obtain Jerk signals, Columns for  Mean and STD respectivly
fBodyAcc-XYZ
fBodyAccJerk-XYZ
fBodyGyro-XYZ
fBodyAccMag -used the accelerometer
fBodyAccJerkMag
fBodyGyroMag
fBodyGyroJerkMag

Gyro=Measurement Calculated from Gyroscope,
Acc= Measuremetn calculated from Accelerometer
Jerk = the body linear acceleration and angular velocity were derived in time to obtain Jerk signals,

##Transformations:
IMPORTANT!
Before starting run_analysis, the txt files were converted into .csv files in order to make the data loading process easier,
to replicate this process, simply convert the txt from a fixed width file format into a csv before running run_analysis.R!
-Data was taken from this data set and then only the information on Mean and Standard deviation was used.
-Data was then transformed into its means of means and standard deviations by grouping the data by Subject number, and activity name.
-activity number was replaced with discriptive activity names
-Data columns reorganized to reflect tidy dataset principles. 

##The step by step transformations are as follows:
1. Merged the training and the test sets to create one data set.
2. Extracted only the measurements on the mean and standard deviation for each measurement. 
3. Used descriptive activity names to name the activities in the data set
4. Appropriately labeled the data set with descriptive variable names. 
5. From the data set in step 4, created a second, independent tidy data set with the average of each variable for each activity and each subject.

##The Data
Summary of the Data used is as follows below:
Download link:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
==================================================================
Human Activity Recognition Using Smartphones Dataset
Version 1.0
==================================================================
Jorge L. Reyes-Ortiz, Davide Anguita, Alessandro Ghio, Luca Oneto.
Smartlab - Non Linear Complex Systems Laboratory
DITEN - Università degli Studi di Genova.
Via Opera Pia 11A, I-16145, Genoa, Italy.
activityrecognition@smartlab.ws
www.smartlab.ws
==================================================================

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

For each record it is provided:
======================================

- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.

The dataset includes the following files:
=========================================

- 'README.txt'

- 'features_info.txt': Shows information about the variables used on the feature vector.

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

The following files are available for the train and test data. Their descriptions are equivalent. 

- 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

- 'train/Inertial Signals/total_acc_x_train.txt': The acceleration signal from the smartphone accelerometer X axis in standard gravity units 'g'. Every row shows a 128 element vector. The same description applies for the 'total_acc_x_train.txt' and 'total_acc_z_train.txt' files for the Y and Z axis. 

- 'train/Inertial Signals/body_acc_x_train.txt': The body acceleration signal obtained by subtracting the gravity from the total acceleration. 

- 'train/Inertial Signals/body_gyro_x_train.txt': The angular velocity vector measured by the gyroscope for each window sample. The units are radians/second. 

Notes: 
======
- Features are normalized and bounded within [-1,1].
- Each feature vector is a row on the text file.

For more information about this dataset contact: activityrecognition@smartlab.ws

License:
========
Use of this dataset in publications must be acknowledged by referencing the following publication [1] 

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.

Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.
