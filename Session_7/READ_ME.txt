# README.txt

## Project Overview  
This project processes and organizes professor data. It includes tasks such as extracting first and last names, generating initials, and joining course data to professor information.

## Code Sections

### 1. Split Full Name into First and Last Name  
This section splits the professor's full name into two columns: `first_name` and `last_name`.

- Code:
  - Splits the `professor` column into `first_name` and `last_name` using the `str.split()` method.
  
- Output:
  - Adds two new columns: `first_name` and `last_name` to the DataFrame.

### 2. Generate Professor Initials  
This section generates the initials of the professor from the first and last names.

- Code:
  - Extracts the first letter of the `first_name` and `last_name` using `str.extract()` with a regex pattern.
  - Combines both initials into one column `professor_initials`.
  
- Output:
  - Adds a new column `professor_initials` with the professor's initials (e.g., "LK" for Ludmila Kuncheva).

### 3. Extract Last Name  
This section extracts the last name from the `professor` column using a regular expression.

- Code:
  - Uses `str.extract()` with the regex `\s(\S+)$` to capture the last word (last name) from the full name.

- Output:
  - Adds a new column `professor_last_name` with the extracted last name.

### 4. Join Course Data with Professor Data  
This section joins course information with the professor's details.

- Code:
  - Joins `df` (professor data) with `df_courses` (course data) on the `professor` column.
  
- Output:
  - Combines the `professor` details with the `courses` data, showing each professor’s course.

## Running the Code

1. Ensure the required data (professors and courses) is in the specified format.
2. Run the script. It will process the professor data, split names, extract initials, and join course data.

## Requirements  
- Python 3.x  
- Pandas module (`pip install pandas`)