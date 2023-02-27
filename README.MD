# [National Park Trails Dashboard](https://public.tableau.com/app/profile/jordan.harilal/viz/NationalParkTrails_16774518911070/NationalParkTrails?publish=yes)



As an avid hiker, I love to travel and explore new trails across the United States and
have a bucket list item to visit every national park in the nation.

In this project, I aim to analyze trails and determine which are considered the best, 
and how different qualities of the trail affect reviews. As an individual who prefers
medium-to-hard difficulty and the reward of a beautiful peak, there's many factors to 
consider, and I don't want to make my judgements solely based off of visitor review.
Vice versa, there may be rewarding trails or local icons that don't fit my desired 
criteria, but that I would likely thoroughly enjoy.

The following is a high-level overview of all the actions taken to achieve this. In the 
"SQL History" file, there is a history of most of the SQL queries ran to convert
the CSV file into relational database.

1. Construction of a DBMS
    - Data modelling in Entity-Relationship Model
        - Importing a CSV to PostGreSQL
        - Creating entity tables TRAIL, PARK, and TRAILREVIEW
        - Designated primary keys
        - Connected TRAIL and PARK via foreign key
        - Connected TRAIL and TRAILREVIEW via foreign key

    - Creating relational tables in SQL
        - Cleaning "country" attribute
        - Cleaning "state" attribute
        - Combining redundant national park names
        - Split 'geoloc' into latitude, longitude
        - Standardizing the unit to imperial system over metric for 'Hawaii' trails

    - Reconstructing attributes to follow ER specifications
        - Split 'geoloc' into latitude, longitude
        - Exploding multi-valued attributes ['features', 'activities'] into their own table
        - Creating a "gain_per_foot" attribute

2. Data Exploration in SQL
    - Understanding the distributions of data

    - Generating questions to maximize the experience in national parks
        - Where are the most parks located?
        - Which parks are the most popular?
        - What parks are considered to have the best trails?
        - Who is the typical reviewer and what activites and features do they prefer?
        - How do the most popular trails compare in difficulty?
        - What is difficulty's relationship with elevation gain and length?
        

2. Data Storytelling in Tableau

