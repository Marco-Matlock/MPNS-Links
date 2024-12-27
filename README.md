# Google Apps Scripts

**MPNS-Hyperlink-Extractor**
This is used to get the hyperlink of plants from the MPNS database.

1. On the active sheet, you must have the names of each plant you would like the hyperlink to. Put it on Column 1.
2. As it processes, it will delete the plant names starting from the bottom and put it onto Sheet 2 (This is to preserve the order when you run it again to get the MPNS Codes as it will read bottom up).
3. Every 4.5 minutes, it will pause, but it will continue running again after a minute until it will hit the Google Apps Scripts recall limit for the day.
4. If you hit the limit for the day, it will still process but it won't get the link.

**MPNS-Code-Extractor**

This is used to get the MPNS code after getting the hyperlinks of the plants from the MPNS database.

1. Stay on the hyperlink page before running this process.
2. Run the apps script and it will stop automatically when it hits the limit.
3. It will keep track of where it left off so there is no need to shift, just run it again until it finishes all the codes.

>>Known Issues
1. For MPNS Code Extractor, sometimes, it will leave 1 empty row behind when you run the process again. Or it will double up on one of the cells. The margin of error here is if you leave it all towards the end, there will be X extra rows based on how many times you had to process. I just manually shifted the rows everytime I processed. Alternatively, you can ignore all of this and leave it at the end. Once everything is processed, copy and paste the original plants list on a third column and adjust everything on column A and B manually to line it all up which is what I usually do and it took me about 10 minutes for a sheet of 12K plants.
