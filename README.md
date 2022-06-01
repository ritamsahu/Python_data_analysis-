Gene Expression Data & presidential election polls





Python Programming Assignment Problem 1: Gene Expression Data


In this problem we will be using agene expressiondata set obtained from a microarray experiment Read more about the specific experiment here. There are two data sets we will use:
The gene expression intensities where the rows represent the features on the microarray (e.g. genes) and the columns represent the different microarray samples.
A table that contains the information about each of the samples (columns in the gene expression data set) such as the sex, the age, the treatment status, the date the samples were processed. Each row represents one sample.
Data:
A gene expression data set called exprs_GSE5859.csv and sample annotation table called sampleinfo_GSE5859.csv
Questions:
1. Read in the two files from Github: exprs_GSE5859.csv and sampleinfo_GSE5859.csv as pandas DataFrames called exprs and sampleinfo. Use the gene names as the index of the exprs DataFrame.
2. check if order of the columns in the exprs DataFrame match the order of the filename in the sampleinfo DataFrame using the == Boolean operator.
3. the columns in the exprs DataFrame are out of order compared to the order of the rows in the sampleinfo DataFrame. To check if there are any columns in the correct order, test for which columns are equal to the filename in the sampleinfo DataFrame.
4. Now, we want to re-order the columns in the exprs DataFrame to match the order of the file names in the sampleinfo DataFrame. One way of doing this is to use the list.index() method. First, we convert the file names in sampleinfo and the column names of exprs and to two lists: a and b. Then, we use a list comprehension to iterate through each element in a and return the index in b that matches using the list.index() method. Once we know all the indexes, we can re-order exprs so that the columns match the same order as the filenames in sampleinfo.
5. Print the head of the two tables: exprs and sampleinfo.
6. Extract the year and month as integers from the sampleinfo table.
7. Convert the dates in the date column from the sampleinfo table into days since October 31, 2002. Add a column to the sampleinfo DataFrame titled elapsedInDays containing the days since October 31, 2002. Show the head of the sampleinfo DataFrame which includes the new column.
8. subset the the sampleinfo DataFrame to include only the CEU ethnicity. Call this new subsetted DataFrame sampleinfoCEU. Show the head of sampleinfoCEU DataFrame.
9. subset the exprs DataFrame to only include the samples with the CEU ethnicity. Name this new subsetted DataFrame exprsCEU. Show the head of the exprsCEU DataFrame.
   
 10. Check to make sure the order of the columns in the exprsCEU DataFrame matches the rows in the sampleinfoCEU DataFrame.
11. Compute the average gene expression intensity in the exprsCEU DataFrame across all the samples. For each sample in the exprsCEU DataFrame, subtract the average gene expression intensity from each of the samples. Show the head of the mean normalized gene expression data.




Problem 2: Is there a pollster bias in presidential election polls?


You will use the polls from the 2012 Presidential Elections to determine (1) Is there a pollster bias in presidential election polls? and
(2) Is the average of polls better than just one poll?
The HuffPost Pollster contains many political polls. You can access these polls from individual races as a CSV but you can also access polls through the HuffPost Pollster API to access the data.
Data:
Polls from the 2012 Presidential Election: Barack Obama vs Mitt Romney. The polls we will use are from the Huffington Post Pollster.
Questions:
1. Read in the polls from the 2012 Presidential Election: Barack Obama vs Mitt
Romney into a pandas DataFrame called election. For this problem, you may read in the polls for this race directly using the CSV file available from the HuffPost Pollster page.
2. How many polls were conducted in November? Define this number as M.
3. What was the median of the number of observations in the November polls? Define this quantity as N.
4. Using the median sample size N from above question, simulate the results from a single poll: simulate the number of votes for Obama out of a sample size N where p = 0.53 is the percent of voters who are voting for Obama.
5. suppose we run M polls where M is the number of polls that happened in November (calculated in Question 2). Run 1,000 simulations and compute the mean of the M polls for each simulation.
6. What is the distribution of the average of polls?
7. Plot qq-plot which we can compare this distribuiton to a normal distribution.
8. What is the standard error (SE) of the average of polls?
