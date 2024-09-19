# HIPE_Experiment_4_DATA WRANGLING AND DATA VISUALIZATION

This repository contains Python codes for solving the given programming problems for this experiment. Full details of each solution using Python are included in this repository.

### Intended Learning Outcomes:
#### 1. To determine the functions and scripts required for data cleaning and visualization
#### 2. Using and utilizing the many codes and functions to construct a Python application that will be utilized for data visualization and wrangling.

## Instructions: 
 - **Download the ECE Board Exam 2 dataset found on this link: bit.ly/ECEBoardExamDataset and write a Python script/code in the Jupyter Notebook to do the given problems. You may submit your Jupyter notebook in the dedicated submission bin.**
 
### The problem requires: 
1. **Data Wrangling:** Clean and transform the data to create specific data frames, like one containing "Name," "Gender," "Track," and whether "Math<70" with a constant "Hometown."

2. **Data Visualization:** Create visuals (e.g., bar charts, pie charts) to illustrate patterns, trends, and insights in the data.

3. **Storytelling:** Use the visuals and data frames to communicate findings and key observations from the data analysis. 

# 1. ECE BOARD EXAM PROBLEM
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

## Other example: 
![image](https://github.com/user-attachments/assets/ef30b6cb-251a-433e-ab3e-12d0bdf6c24c)
## Output: 
![image](https://github.com/user-attachments/assets/4de76db1-7e54-40ce-941a-493cb9896f20)

# B. Mindy DataFrame 
#### Function - df['Average'] = df[['Math','Electronics', 'GEAS', 'Communication']].mean(axis = 1)

![image](https://github.com/user-attachments/assets/9526906c-3cd4-4793-8cec-cc3e2455b40c)

Description - This line of code computes the average score across the 'Math', 'Electronics', 'GEAS', and 'Communication' columns for each row in the DataFrame and stores the result in a new column called 'Average'. 

- **df[['Math', 'Electronics', 'GEAS', 'Communication']]:** Selects the columns 'Math', 'Electronics', 'GEAS', and 'Communication' from the DataFrame.
- **.mean(axis=1):** Calculates the mean of these columns for each row (axis=1 specifies row-wise operation).
- **df['Average']** = ...: Create a new column, the 'Average' column, in the DataFrame df to store these calculated mean values.

#### Function - mindy = df[(df['Hometown'] == 'Mindanao') & (df['Gender'] == 'Female') & (df['Average'] >= 55)][['Name', 'Track', 'Electronics', 'Average']] mindy (this line must be at the second line)

![image](https://github.com/user-attachments/assets/59c658bd-5f15-4bf7-a0a1-6a7e79e2015f)

Description - This line of code filters the DataFrame df to show only those rows where the 'Average' score is at least 55, the 'Hometown' is 'Mindanao,' and the 'Gender' is 'Female'. It then builds a new Mindy DataFrame with only the filtered rows 'Name, Track, Electronics, and Average' columns.

- **df['Hometown']** **== 'Mindanao'**: Filters rows where the 'Hometown' column equals 'Mindanao'.
- **df['Gender']** **== 'Female'**: Filters rows where the 'Gender' column equals 'Female'.
- **df['Average'] >= 55**: Filters rows where the 'Average' column is greater than or equal to 55.
- The **& operator** combines these conditions to include rows that meet all criteria.
- **[['Name', 'Track', 'Electronics', 'Average']]**: Selects only the columns 'Name', 'Track', 'Electronics', and 'Average' from the filtered rows.
- **mindy =** : Stores the filtered data in a new DataFrame named mindy
- **mindy**: Displays the resulting DataFrame mindy with the filtered data.
## Output: 
![image](https://github.com/user-attachments/assets/99b40f8e-fbee-4063-8ea9-b98cd0000868)

## Other example: 
![image](https://github.com/user-attachments/assets/378dca6f-b2b6-428c-b036-89f502533c90)
## Output: 
![image](https://github.com/user-attachments/assets/04995fc2-ed9b-4047-9add-5c037e22e577)

# 2. Creating Visualization that shows how the different features contributes to average grade.
#### Library - import matplotlib.pyplot as plt

![image](https://github.com/user-attachments/assets/d29e865e-da03-41a5-9154-328965e19b97)

Description - A MATLAB-like interface for making several kinds of static, interactive, and animated visualizations in Python is provided by the matplotlib.pyplot module in the Matplotlib toolkit. It is extensively utilized for creating 2D plots and figures, including scatter plots, bar charts, and line graphs.

#### Library - import seaborn as sns 

![image](https://github.com/user-attachments/assets/a25c9664-bdd9-4565-80ad-87686fec1604)

Description - Seaborn is a Matplotlib-based statistical visualization Library that makes it easier to create visually appealing and educational charts like violin plots and heatmaps. It works nicely with Pandas and provides color schemes and themes to improve the story's visual appeal.

### VISUALIZATION BAR PLOT 1
#### Function- df['Average'] = df[['Math', 'Electronics', 'GEAS', 'Communication']].mean(axis=1)

![image](https://github.com/user-attachments/assets/2e9645ed-0a2c-4bb8-896d-80c88c9c7c59)

Description - The average score for each student in math, electronics, GEAS, and communication is calculated on this line. Each row (i.e., each student's score) is averaged using the mean(axis=1) function, and the result is saved in a new column named "Average" in the DataFrame df.

#### Line - plt.figure(figsize=(10, 6)) 

![image](https://github.com/user-attachments/assets/d0fc2798-6c05-40ff-986e-e5c1d3b80cbe)

Description - This line ensures that the plot is clean and suitably scaled for improved visualization by setting the plot's dimensions to 10 inches wide by 6 inches height.

#### Function - sns.barplot(x='Track', y='Average', hue='Gender', data=df) 

![image](https://github.com/user-attachments/assets/18e45d6f-f188-478c-96b2-6399700a6254)

Description - Seaborn creates a bar plot in sns.barplot(x='Track', y='Average', hue='Gender', data=df). Different "Track" categories, such as communication and instrumentation, are represented by the x-axis, while average grades are displayed on the y-axis. Color coding is added via the hue='Gender' parameter to distinguish between the male and female genders inside each track.

#### Function - plt.title('Average grade in terms of Track and Gender')

![image](https://github.com/user-attachments/assets/f04fc6d4-e024-41e3-bfdf-0e00f78a7396)

Description - plt.title('Average grade in terms of Track and Gender'): This defines the plot's title and indicates that it displays average grades broken down into "Track" and "Gender" categories.

#### Line - plt.show()

![image](https://github.com/user-attachments/assets/839a6710-cf86-4c96-ab72-5cea32a38353)

Description - This line renders and displays the plot on the screen.

### VISUALIZATION USING BAR PLOT 2 
#### Function - plt.figure(figsize=(10,6))

![image](https://github.com/user-attachments/assets/d0fc2798-6c05-40ff-986e-e5c1d3b80cbe)

Description - This line ensures that the plot is clean and suitably scaled for improved visualization by setting the plot's dimensions to 10 inches wide by 6 inches high.

#### Function - sns.barplot(x='Hometown', y='Average', hue='Track', data=df)

![image](https://github.com/user-attachments/assets/34b2cfad-f2a2-4f39-94f9-cd4f21880299)

Description - The bar plot displays the average grades on the y-axis and various "Hometown" categories (such as Luzon, Mindanao, and Visayas) on the x-axis. The `hue='Track'} parameter allows you to compare the performance of different tracks in different hometowns by coloring the bars according to 'Track' categories (e.g., Communication, Instrumentation). Data from the DataFrame {df} is used in the visualization.

#### Function - plt.title('Average grade in terms of Hometown and Track')

![image](https://github.com/user-attachments/assets/1136ce6d-2138-4573-89d1-5c7982fb22ee)

Description - Adds a title to the plot, showing the average grades segmented by 'Hometown' and 'Track'.

#### Line - plt.show()

![image](https://github.com/user-attachments/assets/839a6710-cf86-4c96-ab72-5cea32a38353)

Description - This line renders and displays the plot on the screen.

### VISUALIZATION USING BOX PLOTS 
#### Function - plt.figure(figsize=(10,6))

![image](https://github.com/user-attachments/assets/d0fc2798-6c05-40ff-986e-e5c1d3b80cbe)

Description - This line ensures that the plot is clean and suitably scaled for improved visualization by setting the plot's dimensions to 10 inches wide by 6 inches high.

#### Function - sns.boxplot(x = 'Track', y = 'Average', hue = 'Gender', data=df) 

![image](https://github.com/user-attachments/assets/c8971453-f657-4ae5-8afa-c9630d892a81)

Description - The box plot's y-axis displays the average grades, while the x-axis reflects other "Track" categories, such as communication and instrumentation. The `hue='Gender'} parameter allows a comparison of average grade distributions within each track by gender by using color to distinguish between genders (e.g., male and female). The DataFrame {df} is the source of the plot's data.

#### Function - plt.title('Distribution of Average Grade in terms of Track')

![image](https://github.com/user-attachments/assets/a99fafb2-085a-420a-87e6-a31227d31123)

Description - Adds a title to the plot, indicating that it shows the distribution of average grades across different tracks.

#### Line - plt.show()

![image](https://github.com/user-attachments/assets/839a6710-cf86-4c96-ab72-5cea32a38353)

Description - This line renders and displays the plot on the screen.

### VISUALIZATION USING SCATTER PLOT 
#### Function - plt.figure(figsize=(10,6))

![image](https://github.com/user-attachments/assets/d0fc2798-6c05-40ff-986e-e5c1d3b80cbe)

Description - This line ensures that the plot is clean and suitably scaled for improved visualization by setting the plot's dimensions to 10 inches wide by 6 inches high.

#### Function - sns.scatterplot(x = 'Electronics', y = 'Average', hue = 'Gender', style = 'Track', data = df, s = 100)

![image](https://github.com/user-attachments/assets/c8a98ed4-2247-48a7-be26-3ed604e0e117)

Description - 'Electronics' scores are plotted on the x-axis of the scatter plot, while average grades are plotted on the y-axis. Gender-specific colors and distinct marking styles are applied to the points for every 'Track' category. The DataFrame {df} is used to provide the plot's data, and 100-sized markers are used to increase visibility.

#### Function - plt.title('Scores in Electronics V.S Average Grade')

![image](https://github.com/user-attachments/assets/e4411992-cada-4d53-ae2d-e303bba88bea)

Description - Adds a title to the plot, indicating that it visualizes the relationship between 'Electronics' scores and average grades.

#### Line - plt.show()

![image](https://github.com/user-attachments/assets/839a6710-cf86-4c96-ab72-5cea32a38353)

Description - This line renders and displays the plot on the screen.

# QUESTION: Does chosen track in college, gender, or hometown contributes to a higher average score? 
- The small differences in average grades across the categories—track (Communication, Instrumentation, Microelectronics), gender (Female, Male), and hometown (Luzon, Mindanao, Visayas)—indicate that all groups achieved similar scores, with averages in the 60s. The graphs suggest that factors like track, gender, and hometown do not significantly affect average scores.







































