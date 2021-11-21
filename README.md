# Movies-ETL

## Movie ETL Overview

This project is to extract, clean and load three movie files into PostgresSQL Database using Python functions and regular expressions.
* inspecting the data
* read and perform cleaning on the data using regular expressions
* merge data
* creating data frames
* load data 

The intended use of this data is clean data for use in a Hackathon. This techincal analysis will be primarily focused on techniques for extracting, cleaning, relating, merging, and loading the data into a database for future reuse.

### Objective 1: Create a function to read three data files
1. Create an ETL function to read the three files
2. Read the data in the Pandas DataFrames
3. Open the Wikipedia JSON file and use the json.load() function to convert the JSON data to raw data
4. Read in the raw Wikipedia movie data as a Pandas DataFrame
5. Return the three DataFrames
6. Set variable for using function
7. Set the DataFrames from the return statement equal to the file names 
### Objective 2: Extract and clean Wiki movie data
1. Create a function to clean the three files
2. Write a list comprehension that filters out TV shows from the Wiki file
3. Read in the cleaned movies list as a DataFrame
4. Create a try-except block that catches errors while extracting the IMDb IDs with a regular expression string and dropping an ID duplicates capturing and printing any exceptions
5. Write a list comprehension to keep the columns that have non-null values from the Wiki DataFrame
6. Create code to clean box office data, convert it to currency, and add it to a DataFrame
7. Create code to clean release date data and add it to a DataFrame
8. Create code to clean running time data and add it to a DataFrame
9. Create a path to each of the Wikipedia, Kaggle metadata, and the MovieLens ratings data files
10. Run the code setting the cleaned Wiki file data to a DataFrame
11. Inspect the DataFrame to ensure the results are as expected
12. Add colunms of Wiki DataFrame to a list and confirm outputed columns
### Objective 3: Extract,clean and merge Kaggle data
1. Combine the code from the previous deliverables
2. Merge the Wiki and Kaggle data ina new DataFrame
3. Drop unnecessary columns from the merged DataFrame
4. Fill in missing Kaggle data using a function created to do so
5. Filter DataFrame to keep necessary columns
6. Rename the columns
8. Use variables to create paths to the 3 data files
9. Set the DataFrames from the return statement equal to the file names
10. Inspect the DataFrames to ensure the results are as expected
### Objective 4: Create the Movie Database and load cleaded data using SQLAlchemy
1. Setup cofig file and import db pasword information from it for the database
2. Change the function so that it doesn't return data to DataFrames and instead creates a connection to the PostgresSQL datat, and adds the cleaned data to the database
3. Change to code os that the variables for the files are passed in the function
4. Create code that prints out the elapsed time to import each row of the rating data.
5. Run the code and verify the table row counts are as expected
### Resources
- Software: Python 3.6.1, Jupyter Notebook, Pandas, Matplotlib, SQLAlchemy, PostgreSQL

## Analysis Results for Movie ETL
1. A summary visualization of these movie results are shown here:

![movie query image](/Resources/movie_query.png)

2. A summary visualization of these ratings results are shown here:

![rating image](/Resources/rating_query.png)

### References:
* wikipedia movie json: https://2u-data-curriculum-team.s3.amazonaws.com/dataviz-online/module_8/wikipedia-movies.json
* The Movie Database (TMDb): https://www.themoviedb.org/
* zip file from Kaggle: https://www.kaggle.com/rounakbanik/the-movies-dataset/download
* RegExr: https://regexr.com/
* RegEx101: https://regex101.com/
* Wikipedia page for "Dash": https://en.wikipedia.org/wiki/Dash
* Verbose RegEx in Python for longer expressions: https://stackoverflow.com/questions/13851794/how-to-implement-a-verbose-regex-in-python
* Introduction to SQLAlchemy: https://www.youtube.com/watch?v=woKYyhLCcnU
* Figma: https://www.figma.com/
* LucidChart: https://www.lucidchart.com/
