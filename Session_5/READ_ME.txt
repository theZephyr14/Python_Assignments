# README.txt

**Project Overview**  
This project processes and organizes annotation files from the `session_4/annotations` directory. The code counts files, organizes them by month, serializes data using JSON and Pickle, and filters annotations based on date.

**Code Sections**  
The code is divided into the following tasks:

1. **Count Files by Month**  
   This section counts the number of annotation files in each month and identifies the month with the highest number of annotations.

   - **Code**:
     - Iterates through the folders in `Annotations_2`, counts the files in each subfolder.
     - Identifies the month with the highest file count.

   - **Output**:  
     - Prints the number of files in each month.
     - Identifies and prints the month with the highest file count.

2. **Organize Annotations by Month**  
   This section organizes annotation files into a dictionary, grouping them by month and year.

   - **Code**:
     - Extracts the date from each filename, converts it to a `datetime` object, and groups files by the month and year.

   - **Output**:  
     - Prints the organized dictionary where each month contains a list of annotation files.

3. **Serialize Data with JSON**  
   This section serializes the organized data using the JSON format.

   - **Code**:
     - Dumps the `annotations_by_month` dictionary into a `JSON` file.
     - Reads the data back from the file and prints it.

   - **Output**:  
     - Saves the dictionary in a JSON file.
     - Prints the loaded JSON data.

4. **Serialize Data with Pickle**  
   This section serializes the data using the Pickle format.

   - **Code**:
     - Dumps the `annotations_by_month` dictionary into a Pickle file.
     - Loads the data back from the Pickle file and prints it.

   - **Output**:  
     - Saves the dictionary in a Pickle file.
     - Prints the loaded Pickle data.

5. **Create Dictionary of Annotations with Date**  
   This section creates a dictionary where each annotation includes the file name and its date.

   - **Code**:
     - Splits filenames to extract the date, creates a dictionary for each month containing filenames and corresponding dates.

   - **Output**:  
     - Prints the dictionary with annotations, where each entry contains the annotation name and its associated date.

6. **Filter Annotations by Date**  
   This section filters annotations that occurred after a specific date, such as July 1st, 2024.

   - **Code**:
     - Filters the annotations dictionary and prints those that have a date later than the specified threshold.

   - **Output**:  
     - Prints annotations that match the date condition.

**Running the Code**  
1. Update file paths to match your local setup.  
2. Run the script. It will process and output the results based on the code sections.

**Requirements**  
- Python 3.x  
- Modules: `os`, `json`, `pickle`, `datetime`
