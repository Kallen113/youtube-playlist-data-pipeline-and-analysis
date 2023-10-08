# youtube-data-pipeline-and-analysis
Data pipeline and analysis of Youtube data, such as playlists 

Step 0:
To get access to our own personal Youtube playlist data (ie, from one's own personal account), we must first access Google Takeout. Access the following URL:  <https://takeout.google.com/settings/takeout>. On this page, be sure to select "YouTube and YouTube Music", and then you will receive an email containing a zipped file comprising 1 or more CSV files.


Step 1: SQL database setup
For this project, we will first create a SQL database & table, in which we will store the data. 

Step 2: Data cleaning

Iterate through the CSV files containing the Youtube data. Create a new column comprising the Youtube URL. This is actually fairly straightforward since the CSV files already have the unique video IDs. 

Second, we need to take the CSV file names, and create a new column--say "video_category"--so that we can include the playlist category or playlist name to store in the SQL table. 

Finally, with the cleaned & processed data, we will export the data to a single cleaned CSV file in a separate playlists_cleaned_data directory. This way, we can readily import this CSV file, implement just a bit more data cleaning & transformations, and then ingest the data directly into a SQL table. 

This CSV file will be named by today's date, so that we can add additional such files as we grab newer Google Takeout data. 

Step 3: ETL data pipeline:

Finally, we will import the cleaned data from the CSV file contained within the playlists_cleaned_data directory. We will implement an ETL data pipeline in which we perform some additional data cleaning & transformation procedures, such as changing data types as necessary to fit the SQL table data structure and column data types.

Additional Steps:
I need to determine a way to prevent duplicate youtube data from being saved as new CSV files are exported to the playlists_cleaned_data directory. One approach could be to filter the data by date--namely, via the "Playlist Video Creation Timestamp" column, which indicates when a given playlist was created. 
