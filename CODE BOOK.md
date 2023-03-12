## Summary
The data set was collected from the "UCI Human Activity Recognition Dataset" which is available at:

[http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones]

This Code book describes the variables,data and all transformations performed to clean up the data and store 
it in file tidyset.txt.

## Dataset

Tidy data contain 180 row and 82 columns. 

Each subject of the study has 6 rows, each row for every type of physical activity measured. 
Column names:

| Index |           Variables            |  Class  |  Range  | Description                                                                                               |
|-------|--------------------------------| --------|---------|-----------------------------------------------------------------------------------------------------------|
|    1  | subjectId                      | integer |  1 - 2  | Identifies the human subject.                                                                             |
|    2  | activityId                     | integer |  1 - 6  | Identifies the activity.                                                                                  |
|    3  | activityType                   |character|  1 - 6  | WALKING, WALKING UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING                                  |
|    4  | tBodyAcc-mean()-X              | numeric | [-1, 1] | Time domain means for body acceleration on X axis.                                                        |
|    5  | tBodyAcc-mean()-Y              | numeric | [-1, 1] | Time domain means for body acceleration on Y axis.                                                        |
|    6  | tBodyAcc-mean()-Z              | numeric | [-1, 1] | Time domain means for body acceleration on Z axis.                                                        |
|    7  | tBodyAcc-std()-X               | numeric | [-1, 1] | Time domain standard deviations for body acceleration on X axis.                                          |
|    8  | tBodyAcc-std()-Y               | numeric | [-1, 1] | Time domain standard deviations for body acceleration on Y axis.                                          |
|    9  | tBodyAcc-std()-Z               | numeric | [-1, 1] | Time domain standard deviations for body acceleration on Z axis.                                          |
|   10  | tGravityAcc-mean()-X           | numeric | [-1, 1] | Time domain means for gravity acceleration on X axis.                                                     |
|   11  | tGravityAcc-mean()-Y           | numeric | [-1, 1] | Time domain means for gravity acceleration on Y axis.                                                     |
|   12  | tGravityAcc-mean()-Z           | numeric | [-1, 1] | Time domain means for gravity acceleration on Z axis.                                                     |
|   13  | tGravityAcc-std()-X            | numeric | [-1, 1] | Time domain standard deviations for gravity acceleration on X axis.                                       |
|   14  | tGravityAcc-std()-Y            | numeric | [-1, 1] | Time domain standard deviations for gravity acceleration on Y axis.                                       |
|   15  | tGravityAcc-std()-Z            | numeric | [-1, 1] | Time domain standard deviations for gravity acceleration on Z axis.                                       |
|   16  | tBodyAccJerk-mean()-X          | numeric | [-1, 1] | Time domain means for the jerk of body acceleration on X axis.                                            |
|   17  | tBodyAccJerk-mean()-Y          | numeric | [-1, 1] | Time domain means for the jerk of body acceleration on Y axis.                                            |
|   18  | tBodyAccJerk-mean()-Z          | numeric | [-1, 1] | Time domain means for the jerk of body acceleration on Z axis.                                            |
|   19  | tBodyAccJerk-std()-X           | numeric | [-1, 1] | Time domain, standard deviations for the jerk of body acceleration on X axis.                             |
|   20  | tBodyAccJerk-std()-Y           | numeric | [-1, 1] | Time domain, standard deviations for the jerk of body acceleration on Y axis.                             |
|   21  | tBodyAccJerk-std()-Z           | numeric | [-1, 1] | Time domain, standard deviations for the jerk of body acceleration on Z axis.                             |
|   22  | tBodyGyro-mean()-X             | numeric | [-1, 1] | Time domain, means for angular velocity on X axis.                                                        |
|   23  | tBodyGyro-mean()-Y             | numeric | [-1, 1] | Time domain, means for angular velocity on Y axis.                                                        |
|   24  | tBodyGyro-mean()-Z             | numeric | [-1, 1] | Time domain, means for angular velocity on Z axis.                                                        |
|   25  | tBodyGyro-std()-X              | numeric | [-1, 1] | Time domain, standard deviations for angular velocity on X axis.                                          |
|   26  | tBodyGyro-std()-Y              | numeric | [-1, 1] | Time domain, standard deviations for angular velocity on Y axis.                                          |
|   27  | tBodyGyro-std()-Z              | numeric | [-1, 1] | Time domain, standard deviations for angular velocity on Z axis.                                          |
|   28  | tBodyGyroJerk-mean()-X         | numeric | [-1, 1] | Time domain, means for the jerk of angular velocity on X axis.                                            |
|   29  | tBodyGyroJerk-mean()-Y         | numeric | [-1, 1] | Time domain, means for the jerk of angular velocity on Y axis.                                            |
|   30  | tBodyGyroJerk-mean()-Z         | numeric | [-1, 1] | Time domain, means for the jerk of angular velocity on Z axis.                                            |
|   31  | tBodyGyroJerk-std()-X          | numeric | [-1, 1] | Time domain, standard deviations for the jerk of angular velocity on X axis.                              |
|   32  | tBodyGyroJerk-std()-Y          | numeric | [-1, 1] | Time domain, standard deviations for the jerk of angular velocity on Y axis.                              |
|   33  | tBodyGyroJerk-std()-Z          | numeric | [-1, 1] | Time domain, standard deviations for the jerk of angular velocity on Z axis.                              |
|   34  | tBodyAccMag-mean()             | numeric | [-1, 1] | Time domain, Average of means for the magnitude of body acceleration.                                     |
|   35  | tBodyAccMag-std()              | numeric | [-1, 1] | Time domain, Average of standard deviation for the magnitude of body acceleration.                        |
|   36  | tGravityAccMag-mean()          | numeric | [-1, 1] | Time domain, Average of means for the magnitude of gravity acceleration.                                  |
|   37  | tGravityAccMag-std()           | numeric | [-1, 1] | Time domain, Average of standard deviation for the magnitude of gravity acceleration.                     |
|   38  | tBodyAccJerkMag-mean()         | numeric | [-1, 1] | Time domain, Average of means for the magnitude of jerk, of body accelaration.                            |
|   39  | tBodyAccJerkMag-std()          | numeric | [-1, 1] | Time domain, Average of standard deviations for the magnitude of jerk, of body accelaration.              |
|   40  | tBodyGyroMag-mean()            | numeric | [-1, 1] | Time domain, Average of means for the magnitude of angular velocity.                                      |
|   41  | tBodyGyroMag-std()             | numeric | [-1, 1] | Time domain, Average of standard deviations for the magnitude of angular velocity.                        |
|   42  | tBodyGyroJerkMag-mean()        | numeric | [-1, 1] | Time domain, Average of means for the magnitude of jerk, of the angular velocity.                         |
|   43  | tBodyGyroJerkMag-std()         | numeric | [-1, 1] | Time domain, Average of standard deviations for the magnitude of jerk, of the angular velocity.           |
|   44  | fBodyAcc-mean()-X              | numeric | [-1, 1] | Frequency domain means for body acceleration on X axis.                                                   |
|   45  | fBodyAcc-mean()-Y              | numeric | [-1, 1] | Frequency domain means for body acceleration on Y axis.                                                   |
|   46  | fBodyAcc-mean()-Z              | numeric | [-1, 1] | Frequency domain means for body acceleration on Z axis.                                                   |
|   47  | fBodyAcc-std()-X               | numeric | [-1, 1] | Frequency domain standard deviations for body acceleration on X axis.                                     |
|   48  | fBodyAcc-std()-Y               | numeric | [-1, 1] | Frequency domain standard deviations for body acceleration on Y axis.                                     |
|   49  | fBodyAcc-std()-Z               | numeric | [-1, 1] | Frequency domain standard deviations for body acceleration on Z axis.                                     |
|   50  | fBodyAcc-meanFreq()-X          | numeric | [-1, 1] | Mean Frequency of the body acceleration on X axis.                                                        |
|   51  | fBodyAcc-meanFreq()-Y          | numeric | [-1, 1] | Mean Frequency of the body acceleration on Y axis.                                                        |
|   52  | fBodyAcc-meanFreq()-Z          | numeric | [-1, 1] | Mean Frequency of the body acceleration on Z axis.                                                        |
|   53  | fBodyAccJerk-mean()-X          | numeric | [-1, 1] | Frequency domain, means for the jerk of the body acceleration on X axis.                                  |
|   54  | fBodyAccJerk-mean()-Y          | numeric | [-1, 1] | Frequency domain, means for the jerk of the body acceleration on Y axis.                                  |
|   55  | fBodyAccJerk-mean()-Z          | numeric | [-1, 1] | Frequency domain, means for the jerk of the body acceleration on Z axis.                                  |
|   56  | fBodyAccJerk-std()-X           | numeric | [-1, 1] | Frequency domain, standard deviations for the jerk of the body acceleration on X axis.                    |
|   57  | fBodyAccJerk-std()-Y           | numeric | [-1, 1] | Frequency domain, standard deviations for the jerk of the body acceleration on Y axis.                    |
|   58  | fBodyAccJerk-std()-Z           | numeric | [-1, 1] | Frequency domain, standard deviations for the jerk of the body acceleration on Z axis.                    |
|   59  | fBodyAccJerk-meanFreq()-X      | numeric | [-1, 1] | Mean Frequency of the jerk of angular velocity on X axis.                                                 |
|   60  | fBodyAccJerk-meanFreq()-Y      | numeric | [-1, 1] | Mean Frequency of the jerk of angular velocity on Y axis.                                                 |
|   61  | fBodyAccJerk-meanFreq()-Z      | numeric | [-1, 1] | Mean Frequency of the jerk of angular velocity on Z axis.                                                 |
|   62  | fBodyGyro-mean()-X             | numeric | [-1, 1] | Frequency domain, means for the jerk of angular velocity on X axis.                                       |
|   63  | fBodyGyro-mean()-Y             | numeric | [-1, 1] | Frequency domain, means for the jerk of angular velocity on Y axis.                                       |
|   64  | fBodyGyro-mean()-Z             | numeric | [-1, 1] | Frequency domain, means for the jerk of angular velocity on Z axis.                                       |
|   65  | fBodyGyro-std()-X              | numeric | [-1, 1] | Frequency domain, standard deviations for the jerk of angular velocity on X axis.                         |
|   66  | fBodyGyro-std()-Y              | numeric | [-1, 1] | Frequency domain, standard deviations for the jerk of angular velocity on Y axis.                         |
|   67  | fBodyGyro-std()-Z              | numeric | [-1, 1] | Frequency domain, standard deviations for the jerk of angular velocity on Z axis.                         |
|   68  | fBodyGyro-meanFreq()-X         | numeric | [-1, 1] | Mean Frequency of angular velocity on X axis.                                                             |
|   69  | fBodyGyro-meanFreq()-Y         | numeric | [-1, 1] | Mean Frequency of angular velocity on Y axis.                                                             |
|   70  | fBodyGyro-meanFreq()-Z         | numeric | [-1, 1] | Mean Frequency of angular velocity on Z axis.                                                             |
|   71  | fBodyAccMag-mean()             | numeric | [-1, 1] | Frequency domain, Average of means for the magnitude of body acceleration.                                |
|   72  | fBodyAccMag-std()              | numeric | [-1, 1] | Frequency domain, Average of standard deviations for the magnitude of body acceleration.                  |
|   73  | fBodyAccMag-meanFreq()         | numeric | [-1, 1] | Mean Frequency of the magnitude of body acceleration.                                                     |
|   74  | fBodyBodyAccJerkMag-mean()     | numeric | [-1, 1] | Frequency domain, means for the magnitude of jerk, of body acceleration.                                  |
|   75  | fBodyBodyAccJerkMag-std()      | numeric | [-1, 1] | Frequency domain, standard deviations for the magnitude of jerk, of body acceleration.                    |
|   76  | fBodyBodyAccJerkMag-meanFreq() | numeric | [-1, 1] | Mean Frequency of the magnitude of jerk, of body acceleration.                                            |
|   77  | fBodyBodyGyroMag-mean()        | numeric | [-1, 1] | Frequency domain, means for the magnitude of angular velocity.                                            |
|   78  | fBodyBodyGyroMag-std()         | numeric | [-1, 1] | Frequency domain, standard deviations for the magnitude of angular velocity.                              |
|   79  | fBodyBodyGyroMag-meanFreq()    | numeric | [-1, 1] | Mean Frequency of the magnitude of angular velocity.                                                      |
|   80  | fBodyBodyGyroJerkMag-mean()    | numeric | [-1, 1] | Frequency domain, means for the magnitude of jerk, of angular velocity.                                   |
|   81  | fBodyBodyGyroJerkMag-std()     | numeric | [-1, 1] | Frequency domain, standard deviations for the magnitude of jerk, angular velocity.                        |
|   82  | fBodyBodyGyroJerkMag-meanFreq()| numeric | [-1, 1] | Mean Frequency of the magnitude of angular velocity.                                                      |

 