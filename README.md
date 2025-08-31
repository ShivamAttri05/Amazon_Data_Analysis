# 📊 Amazon Product Data Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project performs a complete **Exploratory Data Analysis (EDA)** on an Amazon product dataset (`amazon.csv`).
The goal is to clean, explore, visualize, and derive insights from the dataset, focusing on product prices, discounts, ratings, and categories.

---

## 📂 Dataset

* **Rows:** 1,465
* **Columns:** 16 (product details, pricing, reviews, links, etc.)
* **Important Features:**

  * `discounted_price` – Product’s discounted price (₹)
  * `actual_price` – Product’s original price (₹)
  * `discount_percentage` – Percentage discount applied
  * `rating` – Average customer rating
  * `rating_count` – Number of ratings received
  * `category` – Product category hierarchy

---

## 🛠️ Steps Performed

### 🔹 1. Data Loading & Inspection

* Loaded data using **pandas**.
* Checked dataset shape, column names, data types, and missing values.
* Converted price, discount, rating, and rating\_count from `object` to numeric.
* Missing values were found only in `rating_count` (2 rows).

### 🔹 2. Summary Statistics

* Computed **mean, median, standard deviation, min, max, quartiles** for numeric columns.
* Detected high skewness in prices and rating counts.

### 🔹 3. Visualizations

Each figure was plotted separately for clarity:

* **Histograms** → Showed skewed price & rating distributions.
* **Boxplots** → Revealed many outliers in prices and rating counts.
* **Countplot** → Showed most ratings lie between **3.5–4.5**.
* **Correlation Heatmap** → Strong correlation (`0.96`) between actual & discounted price.
* **Scatter Plots** → Clear linear relation between `actual_price` & `discounted_price`; weak relation between `discounted_price` & `rating`.
* **Bar Plots (Categories)** → Average price comparison across top product categories.

### 🔹 4. Key Insights

* **Price Distribution:** Most products are low–mid range, few very high-priced products act as outliers.
* **Discounts:** Many products have high discounts (>50%), but discount % is slightly lower for expensive items.
* **Ratings:** Clustered around 4.0–4.2, showing generally positive feedback.
* **Rating Count:** Most products have few ratings, but some popular products dominate with 100k+ reviews.
* **Categories:** Electronics and Computers & Accessories dominate both dataset size and pricing.

---

## 📈 Tools & Libraries

* **Python**
* **pandas** – data loading & cleaning
* **numpy** – numeric operations
* **matplotlib** & **seaborn** – visualizations

---

## 📑 How to Run

1. Clone this repo:

   ```bash
   git clone https://github.com/your-username/Amazon_Data_Analysis.git
   cd Amazon_Data_Analysis
   ```
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter notebook:

   ```bash
   jupyter notebook
   ```
4. Open `EDA_Amazon.ipynb` and run all cells.

---

## 🚀 Next Steps

* Investigate extreme outliers in price & rating count.
* Analyze sentiment from `review_content`.
* Build ML models to predict **rating** or **discount percentage**.
* Perform clustering to group products with similar attributes.

---