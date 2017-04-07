# Getting and Cleaning HAR dataset
The repo contains cleaned dataset related to the Human Activity Recognition Using Smartphones. 
URL : http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

# TASK

## Step 1:
- Create a folder "dataset" in the repo folder and extract the downloaded dataset

## Step 2:
- Read the <b>Training</b> & <b>Testing</b> data from the .txt files inside the train and test folders respectively. 
- Each of these data was merged rowwise using rbind() and the columns were renamed. 

## Step 3:
- From the feature list (available in "features.txt" file) features names which denote "mean" and "standard deviation" features were extracted using the grep(). 
- The features names in the raw dataset contained special characters like "(" ,")", "-" which were substitued by "" and "_" using the gsub().

## Step 4:
- The "Activity" data is a set of activities that act as "Labels" for the "Feature Name".
- The raw dataset represents these activities in numbers from 1 to 6 with each number representing an activity name. This mapping was available in "activity_labels.txt" file
- The numeric representation was then changed to the respective activity name and the column was labelled as "labels".

## Step 5: 
- In the final step a tidy_dataset was created from the cleaned dataset. 
- The tidy dataset(available as "tidy.txt") contained the mean values of each variable for each activity and each subject.
