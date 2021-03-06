# Getting and Cleaning Data
Coursera's Getting and Cleaning Data course repository

## Disclaimer

This is a repository for any and all code written for the Getting and Cleaning Data Coursera course through Johns Hopkins University.

## The project

The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected. 

One of the most exciting areas in all of data science right now is wearable computing - see for example [this article](http://www.insideactivitytracking.com/data-science-activity-tracking-and-the-battle-for-the-worlds-top-sports-brand/) . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

## What to do

You should create one R script called run_analysis.R that does the following. 

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names. 
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

Here are the data for the project:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

## Setup

The following steps are needed in order to execute the project

1. Unzip the source (https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip) into a folder on your local drive.
2. Put run_analysis.R into `UCI HAR Datase` on that folder where you unziped the file.
3. In RStudio: setwd("<your_base_folder>\\UCI HAR Dataset\\"), followed by: source("run_analysis.R").
4. Use data <- read.table("tidy_data_with_averages.txt") to read the data.

## Explanation

The script contained in this repository (run_analysis.R) must be run in the same folder as the downloaded data for this project (listed above).

Once executed, the script will generate 2 files:

1. cleaned_merged_data.txt: contains the data merged and cleaned.
2. tidy_data_with_averages.txt: contains the tidy data set with the average of each variable for each activity and each subject

The last one (tidy_data_with_averages.txt) is the expected file to submit for grading.
