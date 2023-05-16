# nosql-challenge
Module 12

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. The editors of a food magazine, Eat Safe, Love, need  to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

Part 1: Database and Jupyter Notebook Set Up

Import the data provided in the establishments.json file   file was imported using Terminal with mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json . 
Named the database uk_food and the collection establishments.
Created an instance of the Mongo Client.
Confirmed that our database is  created.
Listed the databases  in MongoDB. 
Confirmed that uk_food is listed.
Listed the collection(s) in the database to ensure that establishments is there.
Finded and displaied  one document in the establishments collection using find_one and display with pprint.
Assigned the establishments collection to a variable to prepare the collection.

Part 2: Update the Database

Inserted the new halal restaurant opened in Greenwich to the Database.
Finded the BusinessTypeID for "Restaurant/Cafe/Canteen" and returned only the BusinessTypeID and BusinessType fields.
Updated the new restaurant with the BusinessTypeID.
Removed any establishments within the Dover Local Authority from the database.
Used update_many to convert latitude and longitude to decimal numbers.
Used update_many to convert RatingValue to integer numbers.

Part 3: Exploratory Analysis
RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating.
Use count_documents to display the number of documents contained in the result.
Display the first document in the results using pprint.
Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.
Which establishments have a hygiene score equal to 20?
There are 41 establishments with a hygiene score of 20 from the uk_food dataset.
Which establishments in London have a RatingValue greater than or equal to 4?
There are 33 establishment with London as the Local Authority and has a RatingValue greater than or equal to 4.
What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
LocalAuthorityBusinessID                         BusinessName  \
0             PI/000178842                              Iceland   
1             PI/000086506                    Atlantic Fish Bar   
2             PI/000179088              Plumstead Manor Nursery   
3                    14425  Howe and Co Fish and Chips - Van 17   
4             PI/000116619                            Volunteer  

How many establishments in each Local Authority area have a hygiene score of 0? There are 55 documents in the result.

