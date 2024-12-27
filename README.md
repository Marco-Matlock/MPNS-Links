# MPNS-Links
This is used to get the hyperlink of plants from the MPNS database.

1. On the active sheet, you must have the names of each plant you would like the hyperlink to. Put it on Column 1.
2. As it processes, it will delete the plant names starting from the bottom and put it onto Sheet 2 (This is to preserve the order when you run it again to get the MPNS Codes as it will read bottom up).
3. Every 4.5 minutes, it will pause, but it will continue running again after a minute until it will hit the Google Apps Scripts recall limit for the day.
4. If you hit the limit for the day, it will still process but it won't get the link.
