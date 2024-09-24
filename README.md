# ECE2112_PA4: Data Wrangling and Data Visualization

## ECE BOARD EXAM PROBLEM

### 1) Data Frames
Create the following data frames based on the format provided:

Example: Vis = [“Name”, “Gender”, “Track”, “Math<70”]; hometown is constant as Visayas

### Background
These are the steps...
 - Import pandas in the library
   
        import pandas as pd
   
 - Load the file "board2.xlsx"

        pd.read_excel('board2.xlsx')
   
 - Add one new column for the Average of the overall subjects using mean formula

        df['Average'] = (df['Math'] + df['Electronics'] + df['GEAS'] + df['Communication']) / 4

#### a.
 - Filename: Instru = [“Name”, “GEAS”, “Electronics >70”]; where track is constant as Instrumentation and hometown Luzon

        Instru = df.loc[(df['Hometown] == 'Luzon')&(df['Track'] == 'Instrumentation')&(df['Electronics']>70), ['Name', 'GEAS', 'Electronics']]

#### b.
 - Filename: Mindy = [ “Name”, “Track”, “Electronics”, “Average >=55”]; where hometown is constant as Mindanao and gender Female

        Mindy = df.loc[(df['Hometown'] == 'Mindanao')&(df['Gender'] == 'Female')&(df['Average'] >= 55), ['Name', 'Track', 'Electronics', 'Average']]

### 2) Data Visualization
  Create a visualization that shows how the different features contributes to average grade.

### Background
These are the steps...

 - Import Matplotlib in the library

         import matplotlib.pyplot as plt

 - Create a visualization for the Average score of each student in the studies

         plt.figure(figsize = (18,10))
         plt.bar(df['Name'], df['Average'])

  - Create a visualization for the Course Subject of each student

         plt.figure(figsize = (30,20))
         df.plot.bat(x = 'Name', y = ['Math', 'GEAS', 'Electronics', 'Communication'])

### Question to ponder
 1) Does chosen track in college, gender, or hometown contributes to a higher average score?
  
 - No, it does not beacuase average score is a mean of overall course subject which are Math, Electronics, GEAS, and Communication.

   The contributions to the average score can be affect by numerical value which doesn't apply to college, gender or hometown for

   they are only applied for the identifications of the student.

### Files
This is where I set and work on my codes

       PA4.ipynb

 ### Reference
1)
       Data Wrangling in Python.pdf


2)
       Matplotlib Cheat Sheet.pdf


##### The codes and answers in the PA are made by Mycho Tormes
