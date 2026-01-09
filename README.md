# Keith Paper Trading Analysis

I developed this project to analyze my personal paper trading history, focusing on tracking investment patterns and passive income. I processed raw transaction data to calculate committed capital, broker fees, and dividend yields.

### Tools Used

* **Python:** The main language used for data processing and logic.
* **Pandas:** I used this for cleaning, sorting, and grouping the trade data.
* **Matplotlib:** I used this library to generate charts for portfolio distribution and cash flow.
* **Jupyter Notebook:** This was the environment I used to build and document the analysis.

### Step-by-Step Methodology

**1. Data Loading and Cleaning**
I started by importing the raw CSV file and converting the date column into a datetime format. This allowed me to sort the trades chronologically and ensure the timeline was accurate for time-series analysis.

**2. Filtering Transactions**
I separated the data into two main groups: purchases and dividends. To maintain data integrity, I used the `.copy()` method when creating these new tables. This is a critical step in Pandas to avoid SettingWithCopyWarnings and ensure that changes to the filtered data do not accidentally modify the original master list.

**3. Grouping and Aggregating**
Using the `.groupby()` function, I consolidated individual transactions for each stock. This allowed me to transform dozens of small trades into a summary of the total dollar amount invested in each company and the total dividends each company has paid out.

**4. Performance Metrics**
I calculated the dividend yield for each stock by comparing total dividends against the absolute value of the investment. This shows which holdings are providing the best return relative to their cost. I also calculated the net income by accounting for broker fees against total dividends.

**5. Data Visualization**
I created two main visualizations to help interpret the results:

* **Portfolio Distribution:** A horizontal bar chart identifying my largest holdings and concentration risks.
* **Investment Timeline:** A cumulative line chart showing the total capital deployment over time.

### Key Results

* **Total Invested:** ~$171,584
* **Dividends Earned:** $557.31
* **Net Profit (Dividends minus Fees):** $469.26

---

### Charts

**Portfolio Distribution**

<img width="648" height="470" alt="image" src="https://github.com/user-attachments/assets/eaf66d39-30e4-4328-824a-6bb7a61387a4" />

**Investment Timeline**

<img width="903" height="452" alt="image" src="https://github.com/user-attachments/assets/7236a3ba-f8e7-4bf9-ab56-cdd825c29736" />
