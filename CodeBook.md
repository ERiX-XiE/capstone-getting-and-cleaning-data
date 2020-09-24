***** to part 1 peer reviewers: I really think the original variable names are descriptive enough, so I only modified a tiny bit *****

This is a code book that describes the variables, the data, and any transformations or work that I performed to clean up the data 
This code book is for "second_tidy_dataset.csv" or "second_tidy_dataset.txt"

In short, this data set summarises the average value for each variable, for each subject/person and each activity

#################### For variable names: ####################

subject, {1~30}, denotes the person whom the observations/rows are about
activity, {WALKING WALKING_UPSTAIRS WALKING_DOWNSTAIRS SITTING STANDING LAYING}, denotes the activity type that the subject(person) performs

########### for the rest of the variable names: ###########

  used prefix 't' to denote time and 'f' to indicate frequency domain signals
  suffix '-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

variable names may contain:
    mean(): Mean value
    std(): Standard Deviation
    those containing "mean" without parenthesis: I just don't know if I should include them, so just included to be safe

the body linear acceleration and angular velocity were derived in time to obtain 
Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional 
signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag)

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing
fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. 

thus, the full list of variables, is:
tBodyAcc-XYZ  (separated into 3 variables ending with X,Y,Z. The same applies to all others)
tGravityAcc-XYZ
tBodyAccJerk-XYZ
tBodyGyro-XYZ
tBodyGyroJerk-XYZ
tBodyAccMag
tGravityAccMag
tBodyAccJerkMag
tBodyGyroMag
tBodyGyroJerkMag
fBodyAcc-XYZ
fBodyAccJerk-XYZ
fBodyGyro-XYZ
fBodyAccMag
fBodyAccJerkMag
fBodyGyroMag
fBodyGyroJerkMag

Here're also other somewhat EXTRA variables that contain the key word "mean" so that I kept them, just in case to be safe
angle(tBodyAccMean,gravity)         
angle(tBodyAccJerkMean),gravityMean)
angle(tBodyGyroMean,gravityMean)
angle(tBodyGyroJerkMean,gravityMean)
angle(X,gravityMean)          
angle(Y,gravityMean)                 
angle(Z,gravityMean)

#################### For variable values: ####################

except the  "subject" and "activity" columns on the leftmost, the values in all other entries are the "average value" for each variable for the 
specific subject & activity indicated in each row 
