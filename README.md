# Retail Customer Behavior Analysis

An end-to-end data analytics project that examines consumer shopping behavior to uncover purchase drivers, optimize marketing effectiveness, and improve customer retention strategies. This project leverages Python for data preprocessing and analysis, SQL for complex business queries, and Power BI for interactive visualizations.

## Table of Contents

- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Technologies Used](#technologies-used)
- [Dataset](#dataset)
- [Business Questions Addressed](#business-questions-addressed)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Analysis Workflow](#analysis-workflow)
- [License](#license)

## Project Overview

This project provides comprehensive insights into retail customer purchasing patterns through detailed statistical analysis and data-driven exploration. By analyzing customer demographics, purchase history, product preferences, and behavioral patterns, the analysis delivers actionable insights for:

- Understanding customer segments and their purchasing behaviors
- Optimizing discount and promotional strategies
- Improving product recommendations and inventory management
- Enhancing customer retention and subscription adoption
- Identifying high-value customer segments

## Key Features

- **Data Cleaning & Preprocessing**: Handling missing values, feature engineering, and data standardization
- **Exploratory Data Analysis**: Statistical summaries and distribution analysis of customer behavior
- **Customer Segmentation**: Classification of customers into New, Returning, and Loyal segments based on purchase history
- **Revenue Analysis**: Gender-based, age-group-based, and subscription-based revenue insights
- **Product Performance**: Analysis of top-rated products and categories with discount effectiveness
- **Purchase Pattern Analysis**: Examination of shipping preferences, payment methods, and purchase frequency
- **SQL-based Business Intelligence**: Complex queries for deep-dive analysis
- **Database Integration**: Automated data pipeline to PostgreSQL for scalable querying

## Technologies Used

- **Python**: Core programming language for data analysis
  - pandas: Data manipulation and analysis
  - NumPy: Numerical operations
  - psycopg2-binary: PostgreSQL database adapter
  - SQLAlchemy: Database connection and ORM
- **SQL (PostgreSQL)**: Advanced querying for business intelligence
- **Jupyter Notebook**: Interactive development and analysis environment
- **Power BI**: Data visualization and dashboard creation

## Dataset

The analysis uses a comprehensive retail customer behavior dataset (`retail-customer-behavior.csv`) containing the following attributes:

- **Customer Information**: Customer ID, Age, Gender
- **Product Details**: Item Purchased, Category, Size, Color
- **Transaction Data**: Purchase Amount (USD), Payment Method, Season
- **Behavioral Metrics**: Review Rating, Previous Purchases, Frequency of Purchases
- **Marketing Data**: Discount Applied, Promo Code Used, Subscription Status
- **Logistics**: Location, Shipping Type

**Key Engineered Features**:

- `age_group`: Customer segmentation by age (Young Adult, Adult, Middle-aged, Senior)
- `purchase_frequency_days`: Numerical representation of purchase frequency patterns

## Business Questions Addressed

This analysis provides answers to critical business questions:

1. What is the revenue contribution by customer gender?
2. Which customers use discounts but still spend above average?
3. What are the highest-rated product categories and items?
4. How do shipping preferences affect purchase amounts?
5. What is the spending difference between subscribers and non-subscribers?
6. Which products have the highest discount redemption rates?
7. How can customers be segmented based on purchase history?
8. What are the most popular products within each category?
9. Do repeat buyers tend to subscribe more often?
10. Which age groups contribute the most revenue?

## Project Structure

```
retail-customer-behavior-analysis/
├── retail-customer-behavior-analysis.ipynb    # Main Jupyter notebook for Python analysis
├── retail-customer-behavior.csv               # Source dataset
├── retail-customer-behavior.sql               # SQL queries for business intelligence
├── README.md                                  # Project documentation
├── LICENSE                                    # License information
└── .gitignore                                 # Git ignore file
```

## Installation

### Prerequisites

- Python 3.7 or higher
- PostgreSQL database (optional, for SQL analysis)
- Jupyter Notebook
- Power BI Desktop (optional, for visualization)

### Setup Instructions

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/retail-customer-behavior-analysis.git
   cd retail-customer-behavior-analysis
   ```

2. **Install required Python packages**:

   ```bash
   pip install pandas numpy psycopg2-binary sqlalchemy jupyter
   ```

3. **Set up PostgreSQL (if using SQL analysis)**:
   - Create a new database named `retail-customer-behavior`
   - Update connection credentials in the notebook:
     ```python
     username = "your_username"
     password = "your_password"
     host = "localhost"
     port = "5432"
     database = "retail-customer-behavior"
     ```

## Usage

### Python Analysis

1. **Launch Jupyter Notebook**:

   ```bash
   jupyter notebook retail-customer-behavior-analysis.ipynb
   ```

2. **Run the notebook cells sequentially** to:
   - Load and explore the dataset
   - Clean and preprocess data
   - Perform feature engineering
   - Generate statistical insights
   - Load data into PostgreSQL

### SQL Analysis

1. **Connect to your PostgreSQL database**:

   ```bash
   psql -U your_username -d retail-customer-behavior
   ```

2. **Execute queries from `retail-customer-behavior.sql`** to generate business insights

### Power BI Visualization

1. Open Power BI Desktop
2. Connect to the PostgreSQL database or import the CSV file
3. Create interactive dashboards based on the analysis findings

## Analysis Workflow

1. **Data Acquisition**: Load the retail customer behavior dataset
2. **Data Quality Assessment**: Identify and handle missing values
3. **Data Transformation**:
   - Standardize column names
   - Create age group categories
   - Map purchase frequency to numerical values
   - Remove redundant features
4. **Exploratory Data Analysis**: Generate statistical summaries and distributions
5. **Database Integration**: Load cleaned data into PostgreSQL
6. **Business Intelligence Queries**: Execute SQL queries for insights
7. **Visualization**: Create dashboards and reports in Power BI
8. **Insights & Recommendations**: Derive actionable business strategies

## License

This project is licensed under the terms specified in the LICENSE file.
