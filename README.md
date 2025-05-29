# Oasis Infobyte Internship Project

## Exploratory Data Analysis of Retail Sales Dataset

The goal of this project was to analyze transactional data from our retail operations to uncover patterns, trends, and actionable insights that can help us make informed business decisions.

Retail businesses thrive on understanding their customers, optimizing inventory, and maximizing sales. With this project, we aimed to answer critical questions such as:

- What are the sales trends over time?  
- Which product categories are driving the most revenue?  
- How do customer demographics influence purchasing behavior?  
- What strategies can we implement to improve performance?

### Recommendations

1. **Focus on High-Performing Product Categories**  
   Insight: Certain product categories (e.g., Electronics, Clothing, and Beauty) contribute significantly more to total sales compared to others.  
   Recommendation:  
   - Allocate more marketing resources and promotions to high-performing categories like Electronics and Clothing, which show consistently higher sales volumes and revenue.  
   - Investigate lower-performing categories to identify potential issues (e.g., pricing, demand, or inventory challenges).

2. **Target Specific Customer Demographics**  
   Insight: Sales patterns reveal that certain demographics (e.g., specific age groups, genders) contribute disproportionately to revenue.  
   Recommendation:  
   - Launch targeted marketing campaigns for males aged 30–50 and females aged 25–45, as these groups exhibit strong purchasing behavior.  
   - Offer personalized discounts or loyalty programs to frequent customers within these demographics.

3. **Optimize Seasonal and Monthly Sales Strategies**  
   Insight: Sales trends indicate fluctuations in revenue across different months, with peaks during certain periods (e.g., holidays or seasonal events).  
   Recommendation:  
   - Plan promotional events and discounts during months with historically lower sales (e.g., February, March) to boost revenue.  
   - Capitalize on peak sales months (e.g., December, October) by increasing inventory for popular products and launching holiday-specific campaigns.

4. **Enhance Product Pricing Strategies**  
   Insight: Products with higher price points (e.g., Electronics priced at 500 or more) generate significant revenue, but lower-priced items (e.g., 25–$50) also contribute substantially due to higher purchase frequency.  
   Recommendation:  
   - Maintain a balanced product portfolio with both premium and affordable options to cater to diverse customer segments.  
   - Experiment with bundling strategies (e.g., combining low-cost items with high-value products) to increase average transaction value.

5. **Improve Customer Retention**  
   Insight: Frequent customers contribute significantly to overall sales, but there may be untapped potential for repeat purchases.  
   Recommendation:  
   - Implement a loyalty program to reward repeat customers and encourage long-term engagement.  
   - Use email marketing or SMS notifications to remind customers about new arrivals, discounts, or abandoned carts.

6. **Analyze Regional and Gender-Specific Preferences**  
   Insight: Gender-based purchasing behavior reveals differences in preferences (e.g., males may prefer Electronics, while females lean toward Beauty products).  
   Recommendation:  
   - Tailor product offerings and advertisements based on gender-specific preferences.  
   - Conduct surveys or focus groups to understand regional preferences and adjust inventory accordingly.

7. **Address Low-Performing Products**  
   Insight: Some products or categories have low sales volumes despite being available in the inventory.  
   Recommendation:  
   - Identify underperforming products and either discontinue them or reposition them through promotions or discounts.  
   - Gather feedback from customers to understand why certain products are less popular and make necessary improvements.

8. **Leverage Data for Predictive Analytics**  
   Insight: Historical sales data provides valuable insights into trends and patterns.  
   Recommendation:  
   - Invest in predictive analytics tools to forecast future sales trends and optimize inventory management.  
   - Use machine learning models to predict customer behavior and recommend products based on past purchases.

9. **Expand Marketing Channels**  
   Insight: While in-store or online sales are strong, there may be untapped opportunities in digital marketing or social media platforms.  
   Recommendation:  
   - Increase investment in social media advertising and influencer partnerships to reach younger demographics (e.g., ages 18–30).  
   - Explore emerging platforms (e.g., TikTok, Instagram Reels) to showcase products and engage with tech-savvy customers.

10. **Monitor and Improve Customer Experience**  
    Insight: Customer satisfaction directly impacts repeat purchases and brand loyalty.  
    Recommendation:  
    - Regularly collect feedback from customers to identify pain points in their shopping experience.  
    - Train staff to provide exceptional service and ensure seamless transactions (both online and offline).

11. **Encourage Cross-Selling and Upselling**  
    Insight: Customers purchasing multiple items or higher-priced products contribute significantly to revenue.  
    Recommendation:  
    - Train sales teams to suggest complementary products during checkout (e.g., pairing Electronics with accessories).  
    - Use algorithms to recommend upsell options (e.g., suggesting a higher-tier product when a customer views a basic model).

12. **Evaluate and Adjust Inventory Levels**  
    Insight: Certain products sell out quickly, while others remain in stock for extended periods.  
    Recommendation:  
    - Use real-time inventory tracking systems to ensure popular items are always in stock.  
    - Reduce overstocking of slow-moving items to free up capital and storage space.

## Data Cleaning of Airbnb NYC 2019 Dataset

The goal of this project was to clean and preprocess the Airbnb NYC 2019 dataset (`AB_NYC_2019.csv`) to ensure its accuracy, consistency, and reliability for downstream analysis or machine learning tasks. Raw datasets often contain issues such as missing values, duplicates, inconsistent formatting, and outliers that can lead to unreliable results if not addressed systematically. By cleaning this dataset, we created a robust foundation for further exploration, visualization, and predictive modeling.

### Purpose of the Project

The primary objectives of this project were:

1. **Ensure Data Integrity:** Verify the accuracy and consistency of the dataset throughout the cleaning process.  
2. **Handle Missing Data:** Address gaps in the data by either imputing missing values or making informed decisions about how to handle them.  
3. **Remove Duplicates:** Eliminate duplicate records to maintain data uniqueness and avoid bias in analysis.  
4. **Standardize Data Formats:** Ensure uniformity in categorical and numeric data formats for accurate analysis.  
5. **Detect and Handle Outliers:** Identify and address extreme values that could skew analysis or model performance.

This cleaned dataset will serve as a reliable input for tasks such as exploratory data analysis (EDA), price prediction models, neighborhood clustering, or market trend analysis.

### Dataset Overview

The dataset contains information about Airbnb listings in New York City for the year 2019. Key attributes include:

- **Listing Details:** Name, host name, neighborhood group, neighborhood, room type.  
- **Geographical Information:** Latitude and longitude.  
- **Pricing Information:** Price, minimum nights, availability.  
- **Review Metrics:** Number of reviews, last review date, reviews per month.

This dataset is prone to issues such as:

- Missing values in columns like `last_review` and `reviews_per_month`.  
- Duplicate records due to repeated entries.  
- Inconsistent formatting in categorical columns (e.g., `neighbourhood_group`, `room_type`).  
- Outliers in numeric columns like price.

### Methodology

**Step 1: Import Libraries and Load Data**  
We began by importing essential libraries such as pandas, numpy, and matplotlib. The dataset was loaded into a Pandas DataFrame for further processing. Since we were working in Google Colab, the file was accessed from Google Drive after mounting it.

**Step 2: Check for Missing Data**  
Missing values were identified using `df.isnull().sum()`. We implemented the following strategies:  
- **Dropped Columns:** Columns like `last_review` and `reviews_per_month` with excessive missing values were dropped.  
- **Imputed Values:** Missing numeric values were filled with the median of their respective columns.

**Step 3: Remove Duplicate Records**  
Duplicate rows were identified using `df.duplicated()` and removed to ensure each record was unique.

**Step 4: Standardize Data Formatting**  
To ensure consistency:  
- Categorical columns were converted to lowercase and stripped of whitespace.  
- Numeric columns were cast to appropriate data types (e.g., `float64` for price, `int64` for minimum_nights).

**Step 5: Detect and Handle Outliers**  
Outliers were detected using the Interquartile Range (IQR) method:  
- Calculated Q1 (25th percentile) and Q3 (75th percentile) for numeric columns.  
- Defined bounds for outliers: `[Q1 - 1.5 * IQR, Q3 + 1.5 * IQR]`.  
- Filtered out rows with outlier values, particularly in the price column.

**Step 6: Save the Cleaned Dataset**  
The cleaned dataset was saved to a new CSV file (`AB_NYC_2019_cleaned.csv`) for future use.

### Challenges Faced

1. **Handling Missing Data:** Deciding whether to drop or impute missing values required careful consideration to preserve data integrity.  
2. **Outlier Detection:** Extreme values in the price column (e.g., listings priced at $10,000+ per night) skewed the distribution. Filtering these outliers was crucial for meaningful analysis.  
3. **Data Standardization:** Ensuring consistent formatting across categorical and numeric columns was challenging but necessary for downstream tasks like modeling.

### Outcome

After completing the cleaning process, the dataset was transformed into a reliable and consistent format. Key achievements include:

- Missing Values Handled: All missing values were either imputed or appropriately dropped.  
- Duplicates Removed: Duplicate records were eliminated, ensuring data uniqueness.  
- Standardized Formatting: Categorical and numeric data were formatted consistently.  
- Outliers Addressed: Extreme values in numeric columns were filtered out to prevent skewing analysis.  
- Clean Dataset Saved: The cleaned dataset was saved as `AB_NYC_2019_cleaned.csv` for future use.

### Applications of the Cleaned Dataset

The cleaned dataset can now be used for various purposes, including:

1. Exploratory Data Analysis (EDA): Visualizing trends in pricing, availability, and neighborhood popularity.  
2. Predictive Modeling: Building models to predict listing prices based on features like location, room type, and reviews.  
3. Market Segmentation: Clustering neighborhoods based on listing characteristics.  
4. Business Insights: Identifying high-demand areas and optimal pricing strategies for hosts.


### Conclusion

This project successfully transformed a raw, messy dataset into a clean and reliable resource for analysis. By addressing key challenges such as missing data, duplicates, and outliers, we ensured the dataset's integrity and usability. The cleaned dataset is now ready for further exploration and modeling, providing valuable insights into the Airbnb market in New York City.


## Wine Quality Prediction

So, this project is all about predicting the quality of wine based on its chemical properties. You know how wine experts can taste a glass of wine and tell you whether it's good or not? Well, what if we could teach a computer to do something similar, but instead of tasting, it uses data about the wine’s chemical makeup? That’s exactly what we’re doing here.

The dataset contains a bunch of chemical properties for each wine sample, like fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol, and more. Each of these columns represents some measurable characteristic of the wine. For example, "alcohol" tells us the alcohol content, "pH" gives us an idea of how acidic or basic the wine is, and so on.

At the end of each row, there’s a column called **quality**. This is what we’re trying to predict—it’s a score that represents how good the wine is, usually on a scale from 3 to 8 or something similar. The higher the number, the better the wine.

### Now, the goal of this project is to build a machine learning model that can take all these chemical properties as input and predict the quality score. It’s like teaching a computer to act as a wine critic, but instead of tasting the wine, it’s analyzing the numbers.

### How I Approach It

1. **Understanding the Data:**  
   First, I spent some time exploring the dataset to understand what each column means and how the features relate to the target (quality). I checked for missing values, looked at the distributions of the features, and even created some visualizations like correlation matrices and pair plots. These helped me see which features might be important in predicting wine quality.

2. **Preparing the Data:**  
   Before feeding the data into any machine learning model, I had to clean and preprocess it. For example, I scaled the features because some models (like Support Vector Machines) work better when all the inputs are on a similar scale. I also split the data into training and testing sets so I could evaluate the model’s performance on data it hadn’t seen before.

3. **Choosing a Model:**  
   I tried several models like Linear Regression, Decision Trees, Random Forest, and Support Vector Machines. Random Forest was a favorite because it handles non-linear relationships well and is pretty robust to noisy data.

4. **Training and Evaluating:**  
   I trained the models on the training set and evaluated their performance using metrics like Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared on the test set. I also tuned hyperparameters using GridSearchCV to get the best performance.

5. **Interpretation:**  
   Finally, I looked at feature importances to understand which chemical properties most strongly influence wine quality. This is valuable for winemakers who want to focus on certain factors to improve their wine.


### Outcome

The best model could predict wine quality with reasonable accuracy, capturing the subtle nuances in the chemical composition that contribute to the wine's perceived quality. It’s not perfect—after all, taste is subjective—but it provides a solid data-driven estimate that could support winemakers or consumers.


