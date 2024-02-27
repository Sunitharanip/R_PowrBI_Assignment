# R_PowrBI_Assignment
This assignment is to analyse, clean and Visualise data using tools using R and Power BI
Introduction
This project focuses on analyzing and visualizing data related to Hollywood movies, including metrics such as profit, worldwide gross, Rotten Tomatoes score, and audience score. The analysis will be conducted using R for data cleaning and preparation, followed by visualization using Power BI.

Data Cleaning in R
1. Data Loading
Use R to load the Hollywood movies dataset from the provided CSV file.
R
Copy code
# Load the dataset
movies_data <- read.csv("hollywood_movies.csv")
2. Data Exploration
Perform an initial exploration of the dataset to understand its structure and contents.
R
Copy code
# View the structure of the dataset
str(movies_data)

# Display summary statistics
summary(movies_data)
3. Data Cleaning
Handle missing values, inconsistencies, and errors in the dataset.
R
Copy code
# Check for missing values
missing_values <- colSums(is.na(movies_data))
print(missing_values)

# Remove rows with missing values
movies_data <- na.omit(movies_data)

![No_of_rows_after_nullValues_removed](https://github.com/Sunitharanip/R_PowrBI_Assignment/assets/156103999/d4a750ea-686c-4488-905e-222fbbbdb2bd)


# Convert data types if necessary
movies_data$Profit <- as.numeric(as.character(movies_data$Profit))
movies_data$Worldwide_Gross <- as.numeric(as.character(movies_data$Worldwide_Gross))
4. Data Transformation
Create additional variables or transformations as needed for analysis.
R
Copy code
# Calculate profit margin
movies_data$Profit_Margin <- movies_data$Profit / movies_data$Worldwide_Gross
5. Export Cleaned Data
Save the cleaned dataset as a new CSV file for further analysis in Power BI.
R
Copy code
# Export cleaned data
write.csv(movies_data, "cleaned_hollywood_movies.csv", row.names = FALSE)


Data Visualization in Power BI
1. Data Import
Open Power BI and import the cleaned dataset (cleaned_hollywood_movies.csv).
2. Data Modeling
Define relationships and create calculated columns or measures as needed.
3. Data Visualization
Utilize Power BI's visualization tools to create insightful charts, graphs, and dashboards.
4. Interactivity
Implement interactive features such as slicers, filters, and drill-downs for dynamic exploration.
5. Dashboard Creation
Design a comprehensive dashboard layout to present the visualizations effectively.

![Dashboard_Films](https://github.com/Sunitharanip/R_PowrBI_Assignment/assets/156103999/58676f7e-8678-445d-8d00-8d41dbb4ddaa)

7. Export and Sharing
Export the Power BI report/dashboard for sharing with stakeholders.
