# README.txt

**Project Overview**  
This project analyzes data from Titanic passenger survival statistics and Netflix movie data. The Titanic data provides insights into survival rates based on passenger attributes like gender and class, while the Netflix data is used for various queries about movie titles, such as counting missing ratings, filtering movies by year and country, and calculating average titles.

**Code Sections**  
The code is divided into the following tasks:

### Titanic Analysis (Titanic Dataset: `train_and_test2.csv`)

1. **Missing Ratings in Netflix Dataset**  
   This section counts the number of missing ratings in the Netflix dataset.

   - **Code**:
     - Uses `df["rating"].isna().sum()` to count missing ratings.
     
   - **Output**:  
     - Prints the total number of missing ratings in the `rating` column of the Netflix dataset.

2. **Movies from India in 2021**  
   This section counts the number of Indian movies released in 2021 in the Netflix dataset.

   - **Code**:
     - Filters the dataset for movies from India released in 2021.
     
   - **Output**:  
     - Prints the number of Indian movies released in 2021.

3. **Movies with Complete Information from 2020**  
   This section filters the dataset to find movies from 2020 with complete information (no missing data).

   - **Code**:
     - Filters the dataset for 2020 movies with no missing data.
     
   - **Output**:  
     - Prints the number of 2020 movies with complete information.

4. **Year with the Most Titles**  
   This section finds the year with the highest number of movie releases.

   - **Code**:
     - Uses `value_counts()` to find the year with the most titles.
     
   - **Output**:  
     - Prints the year with the most movie titles and the count.

5. **Average Number of Titles from 2010 Onwards**  
   This section calculates the average number of movie titles released from 2010 onwards.

   - **Code**:
     - Filters movies released from 2010 onward and calculates the mean of `release_year` counts.
     
   - **Output**:  
     - Prints the average number of titles released from 2010.

### Titanic Passenger Survival Analysis (Titanic Dataset: `train_and_test2.csv`)

6. **Survival Rate by Gender**  
   This section calculates the ratio of male to female survivors and the overall survival percentage by gender.

   - **Code**:
     - Filters the Titanic dataset for survivors (`2urvived` == 1).
     - Counts male and female survivors and calculates the survival ratio between them.
     
   - **Output**:  
     - Prints the survival ratio of males to females among the survivors.
     - Prints the percentage of males and females who survived.

7. **Survival Rate by Class**  
   This section analyzes the survival rate based on passenger class (upper vs. lower, based on fare).

   - **Code**:
     - Computes the mean fare, then splits the dataset into upper and lower classes.
     - Calculates the survival percentage for both upper and lower classes.
     
   - **Output**:  
     - Prints the survival percentage for upper and lower classes.

8. **Survival Rates by Gender**  
   This section calculates and prints the survival rates for male and female passengers.

   - **Code**:
     - Filters for male and female survivors, then computes the survival percentages.
     
   - **Output**:  
     - Prints the percentage of males and females who survived.

**Running the Code**  
1. Ensure all CSV files are located in the correct paths as specified in the script.  
2. Run the script to generate results on Titanic passenger survival statistics and Netflix movie statistics.

**Requirements**  
- Python 3.x  
- Modules: `pandas`, `os`

