# Python-Data-Analysis-Lab
A repository containing Python code for data analysis tasks, including Pandas usage, column creation, concatenation, renaming, reordering, and groupby operations. This code is part of a series of data analytics labs for the course Data 1202: Data Analytics Tools.
## Getting Started

### Prerequisites

Before you begin, ensure you have met the following requirements:

- **Python:** This project is developed using Python [insert your version]. Make sure you have Python installed on your system. You can download it from [python.org](https://www.python.org/).

- **Pandas Library:** This project relies on the Pandas library for data manipulation. Install it using the following command:

  ```bash
  pip install pandas

  ```
  ### Installing

Follow these steps to get your project up and running:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/morayoshafa/your-repo.git
   

2. **Navigate to the Project Directory:**
    ```bash
    cd your-repo


3. **Install Dependencies:**
Run the following command to install the required Python libraries:
    ```bash
    pip install -r requirements.txt

      ```

    ## Running the tests
This code reads a CSV file, sets a default value for a new column, calculates a new column based on existing columns, and demonstrates two methods for dropping columns.
    
       #Expand the number of columns
       pd.set_option('max_columns', 500)

       #Define variables for the csv files, this step is not mandatory but it will help to understand the importing data step in Python
       File_1 = "Salaries.csv"

       # Read the csv file 
       raw_df = pd.read_csv(File_1)

       # Display the first few rows of the dataframe
       raw_df.head()

       # SETTING A DEFAULT COLUMN VALUE
       raw_df["Benchmarks"] = 70000

       # Display the first few rows with the new column
       raw_df.head()

       # CALCULATE A COLUMN
       raw_df["Salary_score"] = round(raw_df["salary"] / raw_df["Benchmarks"], 2)

       # Display the first few rows with the calculated column
       raw_df.head()

       # Display the columns in the dataframe
       print(raw_df.columns)

       # DROPPING a COLUMN
       # Method 1: Subset the dataframe by including only specific columns.
       Subset_raw_df = raw_df[['rank', 'discipline', 'service']]
       Subset_raw_df.head()

       # Method 2: Use the drop method to drop the salary column.
       Subset_raw_df = raw_df.drop(['sex', 'salary'], axis=1)
       Subset_raw_df.head()

       
         
  ### Breakdown of Tests
  
Test 1: 
                                                                                                                                                         This initial test is designed to validate the correct loading of data from the CSV file. It checks whether the script can successfully read the file, ensuring that the dataframe is populated with the expected columns and data.

Purpose:

Verify the script's ability to handle file input.
Confirm that the dataframe has the correct structure and contains the expected initial data.
Ensure the data loading process sets an appropriate foundation for subsequent operations.       


Test 2: 
The second test focuses on the calculation of a default column and its subsequent addition to the dataframe. It ensures that the script correctly sets a default value for a new column and integrates it into the existing dataframe.

Purpose:

Validate the script's capability to add new columns with default values.
Confirm that the default value is applied uniformly to all rows in the dataframe.
Ensure the integrity of the dataframe after the addition of the new default column.


 ## Deployment
 If you want to deploy your data analytics script or share it with others, follow these steps:

1.Packaging the Script:

Package your script and its dependencies. You can use tools like pyinstaller or cx_Freeze to create standalone executables.


2.Providing Instructions:

Include clear instructions on how users can run the script in their own environments.
Specify any configuration settings or parameters that users may need to adjust.


3.Release Notes:

If applicable, provide release notes for each version, outlining changes, new features, or bug fixes.

## Author
Olufunmilola Morayo Shafa

## License
This project is licensed under the MIT License see the LICENSE.md file for details
      
## Acknowledgement
1. Dr Omar Al-Trad
2. Inspiration


                                                                                                                                                         
                                                                                                                                                         
                                                                                                                                                         
       
     

