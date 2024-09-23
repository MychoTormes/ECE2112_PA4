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
   
