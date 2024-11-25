# BabyName_SQL

### Overview

Using MySQL, I conducted a comprehensive analysis on the Baby Names dataset spaning across from 1980 to 2009. I leveraged SQL to uncover this insight from large dataset of more than 2 million rows.

## Steps:

Here's a breakdown of the steps I followed and the insights uncovered:

## 1. Data Loading in SQL:
I got the raw data from Maven Analytics containing 2 files of names and regions. 
- In MySQL, created 2 tables names and regions and inserted data using **Insert INTO** command.
- As there was 2 million rows it cannot directly be inserted in the table. Using below command inserted the data in the table.
  ![image](https://github.com/user-attachments/assets/b44dfa86-4014-4832-be80-f735f0d4d18b)

### Names table preview:
![image](https://github.com/user-attachments/assets/dc369935-d1d3-4924-b93e-d8266b708f05)

### Regions table preview
![image](https://github.com/user-attachments/assets/b8662534-a305-4415-b459-51148081a0fe)

  
## 2. Key Insights
With the data prepared, I conducted exploratory data analysis (EDA) using SQL queries including aggregations, sub-queries, Common Table Expressions and Window Functions

### Objective 1: 

#### Insight 1: Finding the overall most popular girl and boy names and how they have changed in popularity rankings over the years

In pursuit of this, I first found most popular boy and girl across the dataset. Using below queries, it turns out Michael is most popular boy and Jessica is most popular girl name

![image](https://github.com/user-attachments/assets/c68a8c76-6a4d-4970-b745-a23a13fae722)


After finding out the names, using below queries it was discovered how popular Jessica and Michael names were over the years

![image](https://github.com/user-attachments/assets/3752cb04-bda8-4c49-8d3b-950e043af23a)


Results Preview:

![image](https://github.com/user-attachments/assets/724cf5a2-6cd9-489b-a914-dc5bbc7dd210)

We can see that Michael is consistently being one of the most popular names for boy over the years. However, for Jessica, its popularity has declined as we approached 2000s era.


#### Insight 2: Finding the names with the biggest jumps in popularity from the first year of the data set to the last year

![image](https://github.com/user-attachments/assets/b5e5f23f-2a7b-4c31-9741-0e3ae8fc5a27)


Results Preview:

![image](https://github.com/user-attachments/assets/ca525323-b2da-401f-adc6-982c0b9a5f49)

We can see that Colton and Aiden's popularity jumped significantly from 5789 and 5691 to 149 and 109 respectively which is a difference of 5640 and 5582.

----------------------------------------------------------------------------------------------------------------

### Objective 2: 
#### Insight 1: For each year, extracting the 3 most popular girl names and 3 most popular boy names

![image](https://github.com/user-attachments/assets/ff9e99d8-32d6-4168-b060-8bde98934042)


#### Insight 2: For each decade, returning the 3 most popular girl names and 3 most popular boy names

![image](https://github.com/user-attachments/assets/e0b35a9c-d464-4877-9106-e748b9aeea67)


----------------------------------------------------------------------------------------------------------------
### Objective 3: 

#### Insight 1: Returning the number of babies born in each of the six regions 

As no region was assigned to MI, first I inserted MI and assigned it to Midwest region and using UNION appended it in regions table

![image](https://github.com/user-attachments/assets/79c0baa9-1378-42e1-845c-33af7cabaf3d)


#### Insight 2: Returning the 3 most popular girl names and 3 most popular boy names within each region

![image](https://github.com/user-attachments/assets/33c00ef1-475f-4913-bdd0-3c4cbd6a117d)


----------------------------------------------------------------------------------------------------------------

### Objective 4: 

#### Insight 1: Finding the 10 most popular androgynous names (names given to both females and males)

To find the androgynous names, I checked which names have gender counts = 2 i.e. M and F

![image](https://github.com/user-attachments/assets/7b1f74c2-7e1e-45c5-97db-75877999285c)



#### Insight 2: Finding the length of the shortest and longest names, and identifying the most popular short names and long names

![image](https://github.com/user-attachments/assets/9da8aad3-34ac-4985-b007-90359121998c)


#### Objective 4: Insight 3: Finding the state with the highest percent of babies named "Chris"


![image](https://github.com/user-attachments/assets/9b292574-0683-4c9c-bc5f-011e42c38f98)

