# Accenture_Data_Analysis

•	Completed a simulation focused on advising a hypothetical social media client as a Data Analyst at Accenture
•	Cleaned, modelled and analyzed 7 datasets to uncover insights into content trends to inform strategic decisions
•	Prepared a PowerPoint deck and video presentation to communicate key insights for the client and internal stakeholders

# Analysis of Content Categories Based on Popularity

# Objective:
The client requested an analysis of their content categories to identify the top 5 categories with the largest popularity. Popularity is measured by the "Score" given to each reaction type.

# Data Selection:
We identified three relevant datasets:
1. **Reaction**
2. **Content**
3. **Reaction Types**

The selection was based on the following criteria:
- The need to quantify popularity using the "Score" for each reaction type.
- Required data showing the content ID, category, content type, reaction type, and reaction score to calculate the popularity.

# Data Cleaning Process:
1. *Remove Missing Values**:
   - Rows with missing values were removed.
2. **Data Type Adjustments**:
   - Changed data types where necessary to ensure consistency.
3. **Remove Irrelevant Columns**:
   - Columns not relevant to the task were removed to streamline the analysis.

**Contents.csv**:
- **Initial State**:
  - 1000 rows and 6 columns.
  - 199 null values in the URL column.
- **Actions Taken**:
  - Removed the URL column as it is not useful for quantitative analysis.
  - Renamed the "Type" column to "Content Type".
  - Zero null values remained after these adjustments.

**Reactions.csv**:
- **Initial State**:
  - 25553 rows and 5 columns.
  - Null values in User ID and Type columns.
- **Actions Taken**:
  - Deleted the User ID column.
  - Removed rows with null values in the Type column.
  - Changed the data type of the Datetime column from object to datetime64[ns].

# Data Merging:
- Merged the three datasets using the merge function with a left join.
  - **Step 1**: Merged Contents and Reactions tables based on Content ID using VLOOKUP().
  - **Step 2**: Merged the result with Reaction Types based on Reaction Type using SUMIF().

# Results:
Top 5 categories by aggregate popularity score:
1. Animals
2. Science
3. Healthy Eating
4. Technology
5. Food

# Visualizations:
- **Pie Chart**: Shows the distribution of popularity scores among the top 5 categories.
- **Bar Graph**: Illustrates the aggregate popularity scores for the top 5 categories.

--- 

