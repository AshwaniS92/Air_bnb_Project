# Amsterdam Airbnb Data Analysis

This project explores Airbnb listings in Amsterdam using a dataset sourced from [Inside Airbnb](http://insideairbnb.com/amsterdam/), capturing data as of December 6th, 2018. The objective is to identify trends, patterns, and insights into the Airbnb market, including pricing, availability, and customer reviews.

---

## **Dataset Overview**

The dataset comprises approximately 20,000 listings and includes the following files:

1. **`calendar.csv`**: Daily availability and pricing for each listing (365 days ahead).
2. **`listings.csv`**: Key variables for visualizations, including price, location, and host details.
3. **`listings_details.csv`**: 80 additional variables describing listings.
4. **`neighbourhoods.csv`**: Names of Amsterdam neighborhoods.
5. **`neighbourhoods.geojson`**: Geo-spatial data for mapping neighborhoods.
6. **`reviews.csv`**: Review counts and related information.
7. **`reviews_details.csv`**: Full details of customer reviews, suitable for text mining.

---

## **Key Questions Explored**

1. How does the price of listings vary across different neighborhoods in Amsterdam?
2. Is there a correlation between room type (e.g., entire home, private room) and price?
3. What is the relationship between reviews per month and listing price?
4. How does the number of a host’s listings affect reviews and pricing?
5. Which neighborhoods have the highest-priced listings?
6. Can sentiment analysis of reviews provide insights into guest experiences?
7. Does availability correlate with price and review count?

---

## **Data Wrangling and Profiling**

### **Data Cleaning**
- Handled missing values in key columns (`name`, `reviews_per_month`, etc.) by replacing them with placeholders like `unknown`.
- Removed unrealistic outliers (e.g., minimum nights > 1000).
- Removed duplicate entries and unnecessary columns.

### **Dropped Columns**
In compliance with PII regulations, 41 sensitive columns were removed from `listings_details.csv`, including:
- Host details (`host_name`, `host_location`, `host_response_rate`, etc.)
- Internal metadata (`listing_url`, `calendar_last_scraped`, etc.)

### **Missing Data**
- The `comments` column in `reviews_details.csv` had 530 missing values, replaced with `Unknown`.

---

## **Data Limitations**

1. The dataset captures a snapshot from December 6th, 2018, which may not reflect current trends, especially post-COVID.
2. Certain variables (e.g., host details) were removed to maintain privacy, limiting analysis on host-specific behaviors.

---

## **Tech Stack**

- **Python**: For data wrangling, analysis, and visualization.
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Geopandas, Scikit-learn, NLTK.
- **Tools**: Jupyter Notebook for interactive exploration.

---

## **Insights and Outcomes**

### **Trends**
- Pricing trends across neighborhoods.
- Room type influences on customer preferences and pricing.

### **Patterns**
- Correlation between reviews, pricing, and availability.
- Host strategies for pricing and customer engagement.

### **Anomalies**
- Identified outliers in minimum nights and pricing data.

---

## **Ethical Considerations**
1. **Privacy**: Anonymized all personally identifiable information.
2. **Bias Awareness**: Recognized potential biases in reviews and listing data.
3. **Transparency**: Limitations of the dataset were explicitly stated.

---

## **How to Use This Repository**

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/Amsterdam-Airbnb-Analysis.git
