Link to the video:
https://www.youtube.com/watch?v=GFQaEYEc8_8&t=348s

###1NF:

- using row to express order is not permitted
- mixing data types within the same column is not permitted
- having table without a primary key is not permitted (NOTE: a primary key can be a combination of 2 or more columns, especially in a many to many relationship)
- repeating groups are not permitted 

###2NF:

- deletion anomaly
- update anomaly
- insertion anomaly
  
![image](https://github.com/bigchungus2303/NBA_Web_scraping_project/assets/50546395/2601faba-a814-4199-a173-dbf6a3fb816a)

2NF is about how non-key attributes columns relate to the key columns
=> Each non-key attribute must depend on the entire primary key, so the player_rating column is probably belong to a separated table

![image](https://github.com/bigchungus2303/NBA_Web_scraping_project/assets/50546395/0e62860e-0924-4f22-ad7a-6623e6709e9c)

![image](https://github.com/bigchungus2303/NBA_Web_scraping_project/assets/50546395/4c030520-f708-4109-9a6a-4afe8f8e0d43)

###3NF:

![image](https://github.com/bigchungus2303/NBA_Web_scraping_project/assets/50546395/9252e276-481d-4fae-ab33-a1a4cc144c72)

for the inconsistency as in the image, player_rating is depend on player_id but through player_skill_level (transitive dependency) the problem is this is a non key attribute column depends on another non key attribute column (which 3NF forbids)

=> should put the player_skill_levels to another table and as a primary key of that table

![image](https://github.com/bigchungus2303/NBA_Web_scraping_project/assets/50546395/b6f6594c-8886-4506-9370-1d6593b62549)

###4NF

![image](https://github.com/bigchungus2303/NBA_Web_scraping_project/assets/50546395/c323b631-b16c-48ee-805f-3b7afb72451b)

=> again, create another table is the solution.

###5NF:

![image](https://github.com/bigchungus2303/NBA_Web_scraping_project/assets/50546395/83fca233-48dd-408f-b76a-f19d3f8248b6)

In the image above, new brand for Suzy is missing 2 more flavors that she said she also likes.

Solution:

![image](https://github.com/bigchungus2303/NBA_Web_scraping_project/assets/50546395/64b1b88e-0499-4241-88ba-a3bdc066e570)
