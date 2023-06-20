# Unit 2 | Homework Assignment: Automate Your Day Job with Python

## Instructions for both projects:

1. Create a new GitHub repo called `python-homework`. Then, clone it to your computer.
2. In your local git repository, create a directory for both of the Python activities. Use folder names that correspond to the activities: **PyBank** and **PyRamen**.
3. In each folder you just created, add a new file called `main.ipynb`. Remember that to create this file you will need to use JupyterLab to correctly generate the .ipynb file format. This will be the main notebook to run for each analysis.
4. Push the above changes to GitHub.

---
## PyBank Instructions & Notes

### **REFERENCE FILE FOR HOMEWORK:** '/PyBank/main.ipynb'

### **IMPORTANT:** Before testing code, delete the 'FinalResults.txt' file in the 'PyBank' folder.  This will allow you to generate a new .txt file based on results.
---
Utilize this financial dataset in this file: [budget_data.csv](PyBank/Resources/budget_data.csv). This dataset is composed of two columns, Date and Profit/Losses.  Your task is to create a Python script that analyzes the records to calculate each of the following:

* The total number of months included in the dataset.
* The net total amount of Profit/Losses over the entire period.
* The average of the changes in Profit/Losses over the entire period.
* The greatest increase in profits (date and amount) over the entire period.
* The greatest decrease in losses (date and amount) over the entire period

Finally, the final script should print the analysis to the terminal and export a text file with the results.

During this exercise, I referenced the following sites to assist in building my code: 
* Opening CSV file and skipping header: [Stack Overflow](https://stackoverflow.com/questions/14257373/how-to-skip-the-headers-when-processing-a-csv-file-using-python)
* Opening CSV file with DictReader: [Python.org](https://docs.python.org/3/library/csv.html)
* Referencing dictionary values in a list to search through values: [Geeks for Geeks](https://www.geeksforgeeks.org/python-accessing-items-in-lists-within-dictionary/)
* Reference item in dictionary: [Stack Overflow](https://stackoverflow.com/questions/8653516/search-a-list-of-dictionaries-in-python)
* Search function: [Stack Overflow](https://stackoverflow.com/questions/8653516/search-a-list-of-dictionaries-in-python)
* Printing to text file: [PythonTutorial.net](https://www.pythontutorial.net/python-basics/python-write-text-file/)

The code is broken down with pseudocode for easy navigation and explanation of the steps.  Section headers are included in CAPS.  A quality check is included but commented out for reference. 

---

## PyRamen Instructions & Notes

### **REFERENCE FILE FOR HOMEWORK:** '/PyRamen/main.ipynb'

### **IMPORTANT:** Before testing code, delete the 'FinalResults.txt' file in the 'PyRamen' folder.  This will allow you to generate a new .txt file based on results.
---
### Read the Data

Complete the following:

* Read in `menu_data.csv` and set its contents to a separate list object. (This way, you can cross-reference your menu data with your sales data as you read in your sales data in the coming steps.)
  * Initialize an empty `menu` list object to hold the contents of `menu_data.csv`.
  * Use a `with` statement and open the `menu_data.csv` by using its file path.
  * Use the `reader` function from the `csv` library to begin reading `menu_data.csv`.
  * Use the `next` function to skip the header (first row of the CSV).
  * Loop over the rest of the rows and append every row to the `menu` list object (the outcome will be a list of lists).
* Set up the same process to read in `sales_data.csv`. However, instead append every row of the sales data to a new `sales` list object.

### Manipulate the Data

Complete the following:
* Initialize an empty `report` dictionary to hold the future aggregated per-product results. 
  * For each row of the `sales` data, set the following columns of the sales data to their own variables: Quantity and Menu_Item
  * Perform a quick check if the `sales_item` is already included in the `report`. If not, initialize the key-value pairs for the particular `sales_item` in the report. Then, set the `sales_item` as a new key to the `report` dictionary and the values as a nested dictionary containing the following:
* Create a nested loop by looping through every record in `menu`.
  * For each row of the `menu` data, set the following columns of the menu data to their own variables: Item, Price, Cost
  * If the `sales_item` in sales is equal to the `item` in `menu`, capture the `quantity` from the sales data and the `price` and `cost` from the menu data to calculate the `profit` for each item.  Cumulatively add the values to the corresponding metrics in the report.  Else print the message "{sales_item} does not equal {item}! NO MATCH!".
* Write out the contents of the `report` dictionary to a text file. The report should output each ramen type as the keys and `01-count`, `02-revenue`, `03-cogs`, and `04-profit` metrics as the values for every ramen type as shown:

During this exercise, no external sites were referenced for building this code.

The code is broken down with pseudocode for easy navigation and explanation of the steps.  The code is broken down into separate sections for running pieces of code independently.  A quality check is included but commented out for reference. 

---

