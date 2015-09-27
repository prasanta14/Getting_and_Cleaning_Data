# Introduction
The script run_analysis.Rperforms the 5 steps described in the course project's definition.

First, all the similar data is merged using the rbind() function. By similar, we address those files having the same number of columns and referring to the same entities.
Then, only those columns with the mean and standard deviation measures are taken from the whole dataset. After extracting these columns, they are given the correct names.
On the whole dataset, those columns with vague column names are corrected.
Finally, we generate a new dataset with all the average measures for each subject and activity type. The output file is called tidydata.txt, and uploaded to this repository.
#Variables
dataActivityTest, dataActivityTrain, dataSubjectTrain, dataSubjectTest, dataFeaturesTest and dataFeaturesTrain contain the data from the downloaded files.
dataSubject, dataActivity and dataFeatures merge the previous datasets to further analysis.
names(dataFeatures) contains the correct names for the x_data dataset.
A similar approach is taken with activity names through the activities variable.
dataCombine merges data in a big dataset.
Finally, the relevant averages which will be later stored in a .txt file. ddply() from the plyr package is used to apply colMeans() and ease the development.
