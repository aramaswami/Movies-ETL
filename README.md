## Movies-ETL  
We have three data sources for movies information that we need to extract, transform and load. The code is designed to open files, clean up the data, and populate a SQL database.

### Part_1: Extraction  
I defined a new function that takes a json and two csv files as arguments. Note that the code assumes that the wiki data is in json format, and the kaggle and ratings data are in csv file.  

### Part_2: Transformation  
Transformation involves several cleanup steps, including merging data, removing duplicates, filling in gaps, selecting the data source when more than one exists, and deleting unwanted or incomplete columns. This is done with code that perform these steps on the raw data.  

### Part_3: Load to database
I created a SQL database with two tables: (i) movies; and (ii) ratings. The transformed and cleaned-up data is transferred directly to the database with the 'to_sql' method.  

### NOTES: Please note the followinng:
(1) The sources data files were large and github generated a file size error, so I am not sure if all data was uploaded. I've retained the file_dir pointing to my local directory for this reason. Please use local files (and update the file_dir reference) to run the code.  
(2) I commented the sql query to split the ratings input because it took significant time to run; please uncomment to run the code block.  
