# **📈 Exercise 1: Line Plot for Total Profit **

## **🛠 Project Overview**
This project visualizes **total profit per month** using a **line plot** with `Matplotlib`.  
The dataset is stored in **company_sales_data.csv**, and the script reads this data using `Pandas`.  
Users can run this script directly in **Google Colab**, without needing local installations.


## **📁 Folder Structure**
```
exercise_1/
│── company_sales_data.csv  # Dataset file
│── exercise_1.ipynb        # Jupyter Notebook script for Colab
│── README.md               # Documentation file
```


## **🚀 Running the Script in Google Colab**
### **🔹 Steps**
1. **Open Google Colab:** [Google Colab](https://colab.research.google.com/)
2. **Upload the dataset (`company_sales_data.csv`)**  
   - Click the **folder icon** in Colab’s sidebar.  
   - Click **“Upload”**, then select `company_sales_data.csv`.  
3. **Run the following code in a Colab cell**:
   ```python
   import pandas as pd
   import matplotlib.pyplot as plt

   # Load the dataset
   data = pd.read_csv("company_sales_data.csv")

   # Extract total profit and months
   months = data["month_number"]
   total_profit = data["total_profit"]

   # Create a line plot for total profit
   plt.figure(figsize=(10, 5))
   plt.plot(months, total_profit, marker='o', linestyle='-', color='b', label="Total Profit")
   plt.xlabel("Month Number")
   plt.ylabel("Profit ($)")
   plt.title("Total Profit Per Month")
   plt.legend()
   plt.grid(True)
   plt.show()
   ```

✔️ **Press Shift + Enter** to execute the cell, and the line plot will be displayed in Colab! 🎉  


## **📜 Code Explanation**
✅ **Reads data** from CSV using `pandas.read_csv()`.  
✅ **Plots total profit** per month using `plt.plot()`.  
✅ **Adds markers, labels, and grid lines** for better visualization.  


## **⚠️ Common Errors & Fixes**
### **1️⃣ `FileNotFoundError: company_sales_data.csv`**
✅ **Issue:** The dataset is missing or not uploaded.  
✅ **Fix:** **Upload the CSV** using the **folder icon in Colab** before running the script.

### **2️⃣ `ModuleNotFoundError: No module named 'pandas'`**
✅ **Issue:** Missing required libraries.  
✅ **Fix:** Install dependencies using:
   ```python
   !pip install pandas matplotlib
   ```

## **📜 License**
This project is open-source under the **MIT License**. Feel free to modify and distribute.


