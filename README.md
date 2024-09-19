# HIPE_Experiment_4_DATA WRANGLING AND DATA VISUALIZATION

This repository contains Python codes for solving the given programming problems for this experiment. Full details of each solution using Python are included in this repository.

### Intended Learning Outcomes:
#### 1. To determine the functions and scripts required for data cleaning and visualization
#### 2. Using and utilizing the many codes and functions to construct a Python application that will be utilized for data visualization and wrangling.

### Instructions: 
#### - Download the ECE Board Exam 2 dataset found on this link: bit.ly/ECEBoardExamDataset and write a Python script/code in the Jupyter Notebook to do the given problems. You may submit your Jupyter notebook in the dedicated submission bin.

# ECE BOARD EXAM PROBLEM 
#### The problem requires: 
#### 1. Data Wrangling: Clean and transform the data to create specific data frames, like one containing "Name," "Gender," "Track," and whether "Math<70" with a constant "Hometown."

#### 2. Data Visualization: Create visuals (e.g., bar charts, pie charts) to illustrate patterns, trends, and insights in the data.

#### 3. Storytelling: Use the visuals and data frames to communicate findings and key observations from the data analysis. 

#### Library - import pandas as pd 

![image](https://github.com/user-attachments/assets/e64f5883-9f49-4d9a-8145-64aaded82949)


Description - The Pandas Library can be imported with the Python command **import pandas as pd**; this command is sometimes shortened to pd for brevity. Pandas is an effective tool for data analysis and manipulation that offers data structures like DataFrames and Series for effectively handling and processing structured data. Thanks to this import, you can use Pandas features and functions in your code to perform operations like data transformation, analysis, and cleaning.

# A. Instrumentation DataFrame 
#### Function - df = pd.read_csv('board2.csv') df (this df must be at the second line) 

![image](https://github.com/user-attachments/assets/a01bd2a8-6832-4e27-a34f-24f40d27ad83)

Description - The contents of a CSV file called **"board2.csv"** are read into a Pandas DataFrame called **"df"** with the line **df = pd.read_csv('board2.csv')**. The data from the CSV file is loaded into this structured table format using the **pd.read_csv()** function. Every column in the CSV becomes a column in the DataFrame, and every row in the CSV becomes a row in the DataFrame.

The data from the CSV file is displayed in tabular form in the DataFrame on the second line, **df**. This makes it simple to see, examine, and work with the data using Pandas tools.

#### Function - instru_df = df[(df['Track'] == 'Instrumentation')&(df['Hometown'] == 'Luzon')&(df['Electronics'] > 70)][['Name', 'GEAS', 'Electronics']] intru_df (this line must be at the second line) 

![image](https://github.com/user-attachments/assets/80f328b6-2df3-425e-9040-2544e7483d58)

Description - The original DataFrame **(df)** is filtered by this function to show data for individuals in the ****'Instrumentation'** track** whose **hometown is 'Luzon'** and whose **'Electronics' score is higher than 70**. There are just three columns in the generated DataFrame **(instru_df)** that display the information of the people who match the criteria: **"Name," "GEAS," and "Electronics."** It assists in reducing data according to particular specifications, which makes it beneficial for focused analysis or reporting.

- The filtered data is stored in the new DataFrame **instru_df**.
-  **df['Track'] == 'Instrumentation'**: Filters the rows where the "Track" column has the value 'Instrumentation'.
-  **df['Hometown']** == 'Luzon': Filters the rows where the "Hometown" column has the value 'Luzon'.
-  **df['Electronics'] > 70**: Filters the rows where the "Electronics" column has values greater than 70.
-  These conditions are combined by the **& operator**, guaranteeing that only rows that meet every condition are chosen.
## Output:
![image](https://github.com/user-attachments/assets/0ab76204-7897-4d46-864b-adde36e0c5ac)












