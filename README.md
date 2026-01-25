# Employee-Data-Analysis-Project

## Project Overview

This project is a comprehensive Python-based data analysis performed on an employee dataset from ABC Company.
The objective is to preprocess the data, perform exploratory data analysis, generate meaningful visualizations, and derive actionable insights.

The project was completed as a culminating assessment for a Python module and demonstrates practical skills in:

Data preprocessing

Statistical analysis

Data visualization

Business insight generation

## Dataset Information

Source: ABC Company (Internal Dataset)

Rows: 458

Columns: 9

Format: Excel (.xlsx)

Key Columns

Team

Position

Age

Salary

Height (preprocessed)

## Tools & Technologies Used

Python 3

Pandas – data manipulation

NumPy – numerical operations

Matplotlib – data visualization

Seaborn – statistical visualization

## Data Preprocessing

To ensure data consistency and integrity:

The height column was corrected by replacing existing values with random integers between 150 and 180 cm.

A fixed random seed was used to maintain reproducibility.

np.random.seed(42)
df['height'] = np.random.randint(150, 181, size=len(df))

## Analysis Performed

### Employee Distribution by Team

Calculated total employees per team

Computed percentage contribution of each team

Visualized using a bar chart

###Employee Segregation by Position

Grouped employees based on job position

Visualized count distribution using bar plots

### Predominant Age Group Identification

Created age bins

Identified the most common age group

Visualized age distribution

bins = [18, 25, 35, 45, 55, 65]

labels = ['18-25', '26-35', '36-45', '46-55', '56-65']

df['Age_Group'] = pd.cut(df['Age'], bins=bins, labels=labels)

### Salary Expenditure Analysis

Identified:

Team with the highest salary expenditure

Position with the highest salary expenditure

Used group-by aggregation and bar charts

### Age vs Salary Correlation

Computed Pearson correlation

Visualized relationship using a scatter plot

correlation = df['Age'].corr(df['Salary'])

### Visualizations

Each analysis task is supported by clear and appropriate visualizations, including:

Bar charts

Scatter plots

All visualizations were created using Matplotlib, ensuring simplicity and clarity.

### Key Insights (Data Story)

Workforce distribution is uneven across teams, indicating operational concentration.

The majority of employees fall within mid-career age groups, suggesting a stable and experienced workforce.

Certain teams and senior positions account for significantly higher salary expenditure.

A positive correlation exists between age and salary, reflecting experience-driven compensation growth.

These insights can help ABC Company with:

Workforce planning

Salary optimization

Team restructuring decisions

## Project Structure
ABC-Employee-Data-Analysis

│
├── data/
│   └── myexcel.xlsx

│
├── analysis/
│   └── employee_analysis.ipynb

│
├── README.md
└── requirements.txt

## How to Run the Project

Clone the repository

Install required libraries

pip install pandas numpy matplotlib seaborn

Run the analysis script or notebook

python employee_analysis.py


or

jupyter notebook

## Learning Outcomes

Real-world data preprocessing

Exploratory Data Analysis (EDA)

Visualization best practices

Translating data into business insights

## Author

Nihaall
Python | Data Analysis | Visualization
