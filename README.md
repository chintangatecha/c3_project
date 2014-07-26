ReadMe
========================================================

All the data is in UCI HAR Dataset. Simply run the run_analysis.R file and it will spit out tidy_data.txt at the end of the function.

Codebook contains other information on how data is setup and how the datatables were created.

Lets look at what run_analysis.R is actually doing.

Script starts with checking tha packages which willbe used in the script are already present. if it is not then install and use it via require function.

we then read activity labels of the text file for using it as column names
next we extract column names related to mean and standard dviation
Then we extract data from all the relevant txt files and load it into relevant data tables.
we then column bind the train data.
next, we row bind test data with train data. which gives us the whole dataset
we then melt and redo (dcast) the dataset to have it with mean.
Finally we write it to a dataset