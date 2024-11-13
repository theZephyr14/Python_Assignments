Here's the full `README.txt` without the `###` and `***`:

---

# README.txt

Project Overview  
This project processes and organizes satellite annotation files from the `session_4/annotations` directory. It includes tasks such as counting files, verifying filename conventions, analyzing dates, organizing files by month, sorting files, and extracting unique satellite identifiers (SN).

Code Sections  
The code is divided into multiple tasks as outlined below:

1. Count Files Containing "QUICKVIEW_VISUAL"  
This section checks for files containing "QUICKVIEW_VISUAL" in their names within the `session_4/annotations` directory.

- Code:
  - Combines file paths using `os.path.join()`.
  - Checks for files with "QUICKVIEW_VISUAL" in the name and counts them.
  - Displays the total number of files that match the criteria.

- Output:
  - Prints the count of files with "QUICKVIEW_VISUAL".
  - Prints "empty" if no files match the criteria.

2. Verify Filename Format with Regex  
This section uses a regular expression to verify that filenames match a specific format.

- Format:
  - Filenames should follow the pattern: `YYYYMMDD_HHMMSS_SNXX_QUICKVIEW_VISUAL.txt`.

- Code:
  - Compiles a regex pattern and matches each file against it.
  - Identifies files that do not match the expected format.

- Output:
  - Prints the names of files that do not follow the convention.

3. Count Files by Month and Year  
This section creates two dictionaries to count files by month and year based on the date in each filename.

- Code:
  - Extracts the date portion from the filename, converts it to a datetime object, and counts the files by year and month.
  - Finds the month with the highest number of files.

- Output:
  - Displays counts of files per year and month.
  - Identifies the month with the most annotations.

4. Copy Files to Month-Based Subdirectories  
This section organizes files by copying them into subdirectories based on their month of creation.

- Code:
  - Reads each file, extracts the month portion, and defines a target directory.
  - Copies files from the `session_4/annotations` directory to corresponding month subdirectories in `Annotations_2`.

- Output:
  - Prints a message indicating each file has been copied to its corresponding month folder.

5. Sort Files by Date in Descending Order  
This section sorts files by their date in descending order and copies them to a new folder, `Sorted_anno`.

- Code:
  - Sorts files based on the first 15 characters of their name (assumed to be date and time).
  - Copies the sorted files to `Sorted_anno`, creating a chronological archive.

- Output:
  - Prints the sorted list of files from the most recent to the oldest.

6. Identify Unique Satellites (SN) and Count Annotations per Satellite  
This section extracts and counts unique satellite numbers (SN) and identifies the latest annotation.

- Code:
  - Finds satellite numbers (SN) in filenames and counts each unique occurrence.
  - Displays the latest satellite activity based on the sorted file list.

- Output:
  - Prints the total number of unique satellites.
  - Lists the count of annotations per satellite.
  - Shows the latest annotation and its linked satellite.

7. Identify Unique Regions (KM) and Count Files per Region  
This section identifies and counts unique regions (denoted by "KM-") in the filenames.

- Code:
  - Searches for the string "KM-" in each filename.
  - Extracts the region identifier following "KM-" and counts occurrences of each unique region.

- Output:
  - Prints the total number of unique regions.
  - (Optional) Uncomment the provided code to print a detailed count of files per region.

Running the Code  
1. Ensure all files are in the `session_4/annotations` directory.  
2. Run the script. It will generate organized folders and output messages with the results.

Requirements  
- Python 3.x  
- Modules: `os`, `shutil`, `re`, `datetime`, `collections`