# Lab-Importing-Datasets-Laptop-Pricing

# **Hands-on Practice Lab: Importing Dataset - Laptops Pricing**

In this lab, you will practice the process of loading and drawing basic insights on a dataset as learnt through the module. You are being provided with a fresh dataset on 'Laptop Pricing' which will be used for all the practice labs throughout the course.

# Objectives

 - Import a dataset from a CSV file to a Pandas dataframe
 - Develop some basic insights about the dataset

Data Analysis with Python
Cheat Sheet: Importing Data Sets
Package/Method	Description	Code Example
Read CSV data set	Read the CSV file containing a data set to a pandas data frame	
1
df = pd.read_csv(<CSV_path>, header = None) 
# load without header 
df = pd.read_csv(<CSV_path>, header = 0) 
# load using first row as header
Copied!
Note: The labs in this course run in JupyterLite environment. In JupyterLite environment, you'll need to download the required file to the local environment and then use the local path to the file as the CSV_path. However, in case you are using JupyterLabs, or any other Python compiler on your local machine, you can use the URL of the required file directly as the CSV_path.
Print first few entries	Print the first few entries (default 5) of the pandas data frame	
1
df.head(n) #n=number of entries; default 5
Copied!
Print last few entries	Print the last few entries (default 5) of the pandas data frame	
1
df.tail(n) #n=number of entries; default 5
Copied!
Assign header names	Assign appropriate header names to the data frame	
1
df.columns = headers
Copied!
Replace "?" with NaN	Replace the entries "?" with NaN entry from Numpy library	
1
df = df.replace("?", np.nan)
Copied!
Retrieve data types	Retrieve the data types of the data frame columns	
1
df.dtypes
Copied!
Retrieve statistical description	Retrieve the statistical description of the data set. Defaults use is for only numerical data types. Use include="all" to create summary for all variables	
1
df.describe() #default use df.describe(include="all")
Copied!
Retrieve data set summary	Retrieve the summary of the data set being used, from the data frame	
1
df.info()
Copied!
Save data frame to CSV	Save the processed data frame to a CSV file with a specified path	
1
df.to_csv(<output CSV path>)
