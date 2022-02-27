# Hoi4-C.W.S.-Expanded
Based off the amazing work done by u/Vezachs, this version of the Combat Width Simulator adds an option to auto-populate the terrain spread based off the user's selected continent.

Notable Features (Original Work): 

Change the province types you're fighting in.
Change the weights relating to from how many sides you're attacking.
Instead of plotting (combat width penalty) on the y-axis,
(used combat width)*(combat width penalty) is plotted on the y-axis.
This gives a more realistic view of your actual combat power.

Version 2.0
Now includes the overstack penalty, which discourages the use of very small divisions.

Added Features:

User is now prompted to enter the ID associated with the continent of his choice
If the selected ID is valid, the terrain types spread is automatically populated using data from the Paradox Wiki

The numbers should be accurate and were generated using the following steps:
1) Created a CSV file from the list of provinces found at the following link: https://hoi4.paradoxwikis.com/List_of_provinces
2) Created a CSV file from the list of states found at the following link: https://hoi4.paradoxwikis.com/List_of_states
3) Downloaded a CSV file containing all known states and the continent they are located in
4) Imported all 3 CSV files into Microsoft SQl Management Studio
5) Added a terrain_type column in the provinces table 
6) Ran a query to populate the columns using the icon name (i.e. desert.png => Desert) 
7) Ran a query to link each province to it's parent state using state_id 
8) Added a join with the "States & Continents" table using state_name
9) Ran a query to get the count for each terrain type and group by Continent 


