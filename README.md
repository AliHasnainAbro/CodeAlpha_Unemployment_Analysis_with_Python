Unemployment Analysis in India during COVID-19
This project aims to analyze the socio-economic consequences of the COVID-19 pandemic on India's workforce and labor market. Using a comprehensive dataset, this analysis provides insights into unemployment dynamics, employment figures, and labor participation rates across different regions in India during the crisis.

Table of Contents
Problem Statement

Data Source

Key Features

Analysis and Visualizations

Key Findings

Technologies Used

How to Run

Contributing

License

Problem Statement
Unemployment, measured by the unemployment rate (number of unemployed people as a percentage of the total labor force), saw a sharp increase during the COVID-19 pandemic. This analysis sheds light on how unemployment rates, employment figures, and labor participation rates were impacted across various regions of India, aiding in understanding the crisis's effects on the labor market.

Data Source
The dataset used for this analysis is Unemployment in India.csv. This CSV file contains monthly data on unemployment metrics for different states/regions in India.

Key Features
The dataset includes the following columns:

Region: The Indian state or region.

Date: The date of data collection (monthly).

Frequency: Frequency of data collection (Monthly).

Estimated Unemployment Rate (%): The estimated unemployment rate in percentage.

Estimated Employed: The estimated number of employed individuals.

Estimated Labour Participation Rate (%): The estimated labor participation rate in percentage.

Area: Specifies whether the data is from 'Rural' or 'Urban' areas.

After preprocessing, the following columns are available:

Est_Unemp_Rate: Renamed from 'Estimated Unemployment Rate (%)'.

Est_Emp_Rate: Renamed from 'Estimated Employed' and scaled (divided by 1,000,000 and rounded to 2 decimal places).

Est_Labour_Rate: Renamed from 'Estimated Labour Participation Rate (%)'.

Year: Extracted year from the 'Date' column.

Month: Extracted month from the 'Date' column.

Analysis and Visualizations
The Jupyter Notebook (Unemployment in india.ipynb) performs the following key steps:

Initial Data Loading and Inspection:

Loads the dataset using pandas.

Displays the first and last few rows (.head(), .tail()).

Checks the dataset's shape (.shape) and information (.info()).

Checks for and handles missing values by dropping rows with nulls, as their percentage is low (.isnull().sum(), .dropna()).

Data Cleaning and Preprocessing:

Renames columns for clarity (Est_Unemp_Rate, Est_Emp_Rate, Est_Labour_Rate).

Converts the 'Date' column to datetime objects.

Scales the 'Estimated Employed' column to millions for better readability.

Adds 'Year' and 'Month' columns derived from the 'Date' column.

Checks for duplicate rows.

Identifies and handles a typo in the 'Frequency' column, then drops it as it's redundant.

Exploratory Data Analysis (EDA):

Analyzes the distribution of data across 'Rural' and 'Urban' areas.

Calculates and visualizes the average unemployment rate by state.

Visualizes the estimated employment rate by state.

Examines the estimated labor participation rate by state.

Generates a heatmap to visualize correlations between numerical features.

Analyzes unemployment rate trends over months, differentiating between urban and rural areas.

Visualizes the labor participation rate over months for urban and rural areas.

Creates interactive sunburst charts to show the hierarchical breakdown of unemployment rates by region and state.

Key Findings
The analysis reveals several important insights into unemployment in India during the specified period:

Impact of Pandemic: The graphs show a steep decline in labor participation, particularly in urban areas, during the peak of the pandemic, indicating a significant degradation compared to rural areas.

Regional Disparities: There are clear regional variations in unemployment and labor participation rates, highlighting the uneven economic impact across different parts of India.

State-wise Overview: Specific states show higher or lower rates of unemployment and labor force participation, indicating localized economic challenges or resilience.

Technologies Used
Python

Pandas (for data manipulation and analysis)

NumPy (for numerical operations)

Matplotlib (for static plotting)

Seaborn (for statistical data visualization)

Plotly Express (for interactive visualizations, such as sunburst charts)

How to Run
Ensure you have the project files: Make sure Unemployment in india.ipynb and Unemployment in India.csv are in the same directory.

Install the necessary libraries:

pip install pandas numpy matplotlib seaborn plotly

Open the Jupyter Notebook:

jupyter notebook "Unemployment in india.ipynb"

Execute all cells: Run all cells within the notebook to see the data preprocessing steps, analyses, and visualizations.

Contributing
Feel free to fork this repository, contribute to the analysis, or suggest improvements.

License
This project is open-source and distributed under the MIT License.
