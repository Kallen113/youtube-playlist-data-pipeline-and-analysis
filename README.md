# youtube-data-pipeline-and-analysis
Data pipeline and analysis of Youtube data, such as playlists 

Step 0:
To get our own Youtube playlist data, we must first access Google Takeout, and select: <https://takeout.google.com/settings/takeout>. Be sure to select "YouTube and YouTube Music", and then you will receive an email containing a zipped file comprising 1 or more CSV files.


Step 1:
For this project, we will first create a SQL database & table, in which we will store the data. 

Step 2:
Iterate through the CSV files containing the Youtube data. Create a new column comprising the Youtube URL. This is actually fairly easy since the CSV files already have the unique video IDs. 

Second, we need to take the CSV file names, and create a new column--say "video_category"--so that we can include the playlist category or playlist name to store in the SQL table. 


