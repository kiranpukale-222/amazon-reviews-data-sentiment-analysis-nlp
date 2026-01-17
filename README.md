# 📊 Amazon Reviews Data Analysis & Sentiment Analysis

## 📌 Project Overview

This project performs **end-to-end data analysis** on Amazon product review data stored in a **SQLite database**. The goal is to clean raw review data, analyze customer and product behavior, and extract meaningful business insights using **Python, data analysis, visualization, and NLP techniques**.

The project answers key business questions such as:

* Which users should Amazon recommend more products to?
* Which products receive the highest number of reviews?
* How does behavior differ between frequent and non-frequent users?
* Do frequent users write longer reviews?
* What is the overall sentiment of customer reviews?

---

## 📂 Dataset Information

* **Source:** Open-source Amazon reviews SQLite database
* **Table Used:** `REVIEWS`
* **Key Columns:**

  * `UserId`
  * `ProfileName`
  * `ProductId`
  * `Score` (Rating)
  * `Summary` (Short review)
  * `Text` (Full review)
  * `HelpfulnessNumerator`
  * `HelpfulnessDenominator`
  * `Time` (UNIX timestamp)

---

## 🛠️ Technologies & Libraries Used

* **Python**
* **Pandas & NumPy** – Data cleaning and manipulation
* **SQLite3** – Database connection
* **Matplotlib & Seaborn** – Data visualization
* **NLTK & TextBlob** – Sentiment analysis (NLP)

---

## 🧹 Data Cleaning & Preprocessing

### 1️⃣ Handling Invalid Records

* Removed rows where:

  ```
  HelpfulnessNumerator > HelpfulnessDenominator
  ```
* Ensures logical consistency of helpfulness votes

### 2️⃣ Removing Duplicate Reviews

* Dropped duplicate rows using:

  * `UserId`
  * `ProfileName`
  * `Time`
  * `Text`
* Prevents biased or repeated feedback from affecting analysis

### 3️⃣ Datetime Conversion

* Converted UNIX timestamps into `datetime` format for better time-based analysis

---

## 📈 Exploratory Data Analysis (EDA)

### 🔹 Statement 1: User Recommendation Analysis

* Grouped data by `UserId`
* Extracted features:

  * Number of reviews
  * Number of products purchased
  * Average rating given
* Identified **top 10 high-value users** who are ideal candidates for product recommendations

### 🔹 Statement 2: Product Popularity Analysis

* Identified products with **more than 500 reviews**
* Analyzed frequently reviewed products to determine popularity and demand

### 🔹 Statement 3: Frequent vs Non-Frequent User Behavior

* Defined user types:

  * **Frequent users:** Purchased more than 50 products
  * **Non-frequent users:** Purchased 50 or fewer products
* Compared rating distributions between the two groups

---

## ✍️ Review Verbosity Analysis

* Calculated **review length** using word count
* Compared text length between frequent and non-frequent users
* Used box plots to identify distribution and outliers

📌 **Insight:** Frequent users tend to write longer and more detailed reviews

---

## 💬 Sentiment Analysis (NLP)

### 🔹 Methodology

* Used **TextBlob** to calculate sentiment polarity
* Polarity range:

  * `+1` → Positive sentiment
  * `0` → Neutral sentiment
  * `-1` → Negative sentiment

### 🔹 Implementation

* Sampled 50,000 reviews for performance efficiency
* Classified reviews into positive and negative categories
* Identified commonly used words in both positive and negative feedback

---

## 📊 Visualizations

* Bar charts for top users and products
* Line and bar plots for rating distribution
* Box plots for review length comparison

---

## 🎯 Key Business Insights

* High-engagement users can be targeted for personalized recommendations
* Frequently reviewed products are ideal for promotions and inventory planning
* Frequent users provide more detailed feedback
* Majority of reviews show **positive sentiment**, indicating customer satisfaction

---

## 🚀 Conclusion

This project demonstrates practical skills in:

* Real-world data cleaning
* Exploratory data analysis
* Customer behavior analysis
* Data visualization
* Natural Language Processing (Sentiment Analysis)

It reflects how data analytics can support **business decision-making in e-commerce platforms**.

---

## 📌 Future Improvements

* Apply machine learning-based sentiment models
* Perform time-series trend analysis
* Build a recommendation system
* Deploy insights using dashboards (Power BI / Tableau)

---

## 👤 Author

**Kiran**

---

## 📜 License

This project is for educational and learning purposes only.
