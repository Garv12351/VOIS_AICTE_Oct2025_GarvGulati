# Airbnb Open Data Analysis Project

## 📋 Project Overview

This project performs comprehensive data analysis on Airbnb Open Data to uncover valuable insights about property listings, pricing, neighborhoods, hosts, and reviews. The analysis is conducted using Python in Google Colab and addresses 9 key business questions.

---

## 🎯 Project Objectives

The project aims to answer the following questions:

1. **What are the different property types in the Dataset?**
2. **Which neighborhood group has the highest number of listings?**
3. **Which neighborhood group has the highest average prices for Airbnb listings?**
4. **Is there a relationship between the construction year of property and price?**
5. **Who are the top 10 hosts by calculated host listing count?**
6. **Are hosts with higher review scores more likely to receive positive reviews?**
7. **Is there a correlation between the price of a listing and its service fee?**
8. **What is the average review rate number (# stars) for listings, and does it vary based on the neighborhood group and room type?**
9. **Are hosts with a higher calculated host listings count more likely to maintain higher availability throughout the year?**

---

## 🛠️ Technologies Used

- **Python 3.x**
- **Google Colab** (Cloud-based Jupyter Notebook)
- **Libraries:**
  - `pandas` - Data manipulation and analysis
  - `numpy` - Numerical computing
  - `matplotlib` - Data visualization
  - `seaborn` - Statistical data visualization
  - `openpyxl` - Excel file handling

---

## 📁 Project Structure

```
airbnb-analysis/
│
├── README.md                          # Project documentation (this file)
├── airbnb_analysis.py                 # Main Python script
├── data/
│   └── airbnb_data.xlsx              # Your Airbnb dataset (Excel file)
└── outputs/
    ├── visualizations/                # Generated charts and graphs
    └── cleaned_data.csv              # Cleaned dataset (optional export)
```

---

## 🚀 Getting Started

### Prerequisites

- Google Account (for Google Colab)
- Airbnb dataset in Excel format (.xlsx or .xls)

### Installation & Setup

1. **Open Google Colab**
   - Go to [Google Colab](https://colab.research.google.com/)
   - Sign in with your Google account

2. **Create a New Notebook**
   - Click on `File` → `New Notebook`

3. **Copy the Code**
   - Copy the entire Python code from `airbnb_analysis.py`
   - Paste it into a cell in your Colab notebook

4. **Run the Notebook**
   - Click the ▶️ (Play) button or press `Shift + Enter`
   - When prompted, upload your Airbnb Excel dataset

---

## 📊 Features

### 1. **Data Assessment**
- Dataset shape and dimensions
- Column names and data types
- Missing values analysis
- Duplicate detection
- Basic statistical summary

### 2. **Comprehensive Data Cleaning**
- ✅ Removal of duplicate rows
- ✅ Handling missing values (median for numeric, mode for categorical)
- ✅ Standardization of column names
- ✅ Outlier detection and handling
- ✅ Text data standardization
- ✅ Data type conversions
- ✅ Negative price removal

### 3. **Advanced Analysis**
Each question is answered with:
- Detailed statistical analysis
- Data visualizations (bar charts, scatter plots, heatmaps, pie charts)
- Key insights and interpretations
- Correlation analysis where applicable

### 4. **Visualizations**
- Bar charts for distributions
- Pie charts for proportions
- Scatter plots for relationships
- Heatmaps for multi-dimensional analysis
- Line plots for trends
- Horizontal bar charts for rankings

---

## 📈 Expected Outputs

### Question 1: Property Types
- Count of each property type
- Bar chart showing distribution
- Total unique property types

### Question 2: Neighborhood Listings
- Listing count by neighborhood
- Bar chart and pie chart
- Highest neighborhood identification

### Question 3: Neighborhood Pricing
- Average and median prices by neighborhood
- Comparative bar charts
- Highest and lowest priced neighborhoods

### Question 4: Construction Year vs Price
- Correlation coefficient
- Scatter plot with trend analysis
- Average price by construction year

### Question 5: Top Hosts
- Top 10 hosts by listing count
- Horizontal bar chart
- Percentage of total listings

### Question 6: Host Reviews
- Top hosts by review scores
- Horizontal bar chart
- Highest rated host identification

### Question 7: Price vs Service Fee
- Correlation analysis
- Scatter plot with regression line
- Average service fee percentage

### Question 8: Review Rates
- Heatmap of reviews by neighborhood and property type
- Top 5 combinations
- Statistical breakdown

### Question 9: Host Availability
- Correlation between listing count and availability
- Scatter plot and comparison chart
- High vs low listing count analysis

---

## 📖 How to Use

1. **Prepare Your Data**
   - Ensure your Excel file contains Airbnb listing data
   - Common required columns: price, neighborhood, property_type, host_name, reviews, etc.

2. **Run the Analysis**
   ```python
   # The script will automatically:
   # 1. Prompt you to upload your file
   # 2. Perform data cleaning
   # 3. Run all 9 analyses
   # 4. Generate visualizations
   ```

3. **Interpret Results**
   - Review printed statistics and insights
   - Examine visualizations for patterns
   - Use findings for decision-making

---

## 🔍 Data Requirements

Your Excel file should ideally contain these columns (or similar):

| Column Name | Description | Type |
|-------------|-------------|------|
| `price` | Listing price | Numeric |
| `neighborhood` | Neighborhood/area name | Text |
| `property_type` / `room_type` | Type of property | Text |
| `host_name` / `host_id` | Host identifier | Text |
| `number_of_reviews` | Review count | Numeric |
| `review_scores_rating` | Review rating | Numeric |
| `service_fee` | Service fee amount | Numeric |
| `availability_365` | Days available per year | Numeric |
| `construction_year` | Year built | Numeric |
| `calculated_host_listings_count` | Host's listing count | Numeric |

**Note:** The script automatically detects column names with variations!

---

## 🔧 Customization

### Modify Cleaning Parameters

```python
# Adjust IQR multiplier for outlier detection
lower_bound = Q1 - 3 * IQR  # Change 3 to 1.5 for stricter outlier removal
upper_bound = Q3 + 3 * IQR
```

### Change Visualization Colors

```python
# Modify color schemes in plot commands
plt.plot(kind='bar', color='your_color', edgecolor='black')
```

### Export Cleaned Data

```python
# Add this at the end of the script
df_clean.to_csv('cleaned_airbnb_data.csv', index=False)
files.download('cleaned_airbnb_data.csv')
```

---

## 📊 Sample Insights You'll Discover

- **Which neighborhoods are most popular?**
- **What property types dominate the market?**
- **How do prices vary across neighborhoods?**
- **Are newer properties more expensive?**
- **Who are the super-hosts?**
- **What factors influence positive reviews?**
- **How are service fees calculated?**
- **Which combinations get the best reviews?**
- **Do busy hosts maintain availability?**

---

## ⚠️ Troubleshooting

### Common Issues

**1. File Upload Error**
```
Solution: Ensure your file is .xlsx or .xls format
Check file size (Google Colab has upload limits)
```

**2. Column Not Found Warning**
```
Solution: The script auto-detects columns
If warnings appear, check your column names match expected patterns
```

**3. Missing Values After Cleaning**
```
Solution: The script handles this automatically
Review the "Post-Cleaning Assessment" section for details
```

**4. Visualization Not Displaying**
```
Solution: Run the cell again
Ensure matplotlib is properly imported
```

---

## 📝 Best Practices

1. **Data Backup**: Keep a copy of your original dataset
2. **Run Sequentially**: Execute all cells in order
3. **Check Outputs**: Review each section's output before proceeding
4. **Save Results**: Download important visualizations
5. **Document Findings**: Add markdown cells with your observations

---

## 🤝 Contributing

This is a learning project. Feel free to:
- Add new analysis questions
- Improve visualizations
- Enhance data cleaning logic
- Add statistical tests

---

## 📄 License

This project is open-source and available for educational purposes.

---

## 👨‍💻 Author

Created for Airbnb Open Data Analysis

---

## 📞 Support

For questions or issues:
1. Check the Troubleshooting section
2. Review Python/Pandas documentation
3. Consult Google Colab documentation

---

## 🎓 Learning Outcomes

After completing this project, you will:
- ✅ Understand data cleaning techniques
- ✅ Perform exploratory data analysis (EDA)
- ✅ Create professional visualizations
- ✅ Calculate correlations and statistical measures
- ✅ Interpret business insights from data
- ✅ Use Python for data science
- ✅ Work with Google Colab environment

---

## 📚 Additional Resources

- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Matplotlib Gallery](https://matplotlib.org/stable/gallery/index.html)
- [Seaborn Tutorial](https://seaborn.pydata.org/tutorial.html)
- [Google Colab Guide](https://colab.research.google.com/notebooks/intro.ipynb)

---

## 🔄 Updates & Versions

**Version 1.0** - Initial Release
- Complete data cleaning pipeline
- 9 analysis questions
- Comprehensive visualizations
- Detailed documentation

---

**Happy Analyzing! 🎉**

*Remember: Data tells a story - your job is to find it!*
