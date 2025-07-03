# E-Commerce-Product-Price-Prediction

This project aims to build a machine learning model that predicts the optimal selling price of products in an e-commerce environment. By leveraging product metadata, customer engagement metrics, and pricing trends, the model helps in dynamic pricing, improving customer satisfaction, and maximizing revenue.

📌 Problem Statement
Retailers on platforms like Flipkart and Amazon often struggle to price their products competitively while maintaining profitability. This project builds a regression model to predict the final selling price (price1) of a product based on factors like ratings, reviews, platform, category, discounts, and fulfillment status.

📦 Dataset Overview
📄 Rows: 15,730
📊 Features: 16
🔗 Source: Kaggle (custom-curated dataset)
Key Features:
Product Info: Title, platform, category (maincateg)
Customer Engagement: Ratings, number of reviews, 1-5 star breakdown
Pricing Variables: Actual price (actprice1), selling price (price1), offer percentage
Operational Status: Fulfillment indicator

⚙️ Workflow
1. Data Preprocessing
  Handled missing values (mode for categorical, median for numerical)
  Treated outliers using IQR method
  Normalized numerical features using MinMaxScaler
2. Feature Engineering
  Converted categorical variables using one-hot encoding
  Cleaned Offer % column
  Selected relevant features using correlation and domain logic
3. Model Building
  Used Linear Regression to predict product selling price
  Split dataset (80-20) for training and testing
4. Model Evaluation
  R² Score: 0.9266
  RMSE: 0.0747
  High correlation between actual and predicted prices
  Residual analysis confirmed model consistency

📊 Visualizations
Rating vs Price, Review count vs Price
Distribution plots for price and residuals
Correlation heatmap to interpret feature relationships

💡 Key Insights
Actual price and discount are the strongest predictors of final selling price.
Products with higher ratings and reviews tend to be priced higher.
1- and 2-star heavy products often sell at discounted or lower prices.
The model can help detect price anomalies or products with potential fake ratings.

🚀 Business Use-Cases
Dynamic pricing automation
Competitive analysis for new product listings
Flagging pricing manipulation or low-performing listings

🧠 Tech Stack
  Python (Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib)
  Jupyter Notebook
  Regression Modeling
