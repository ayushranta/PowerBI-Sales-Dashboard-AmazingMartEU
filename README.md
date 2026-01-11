# 📊 AmazingMartEU Sales Performance Dashboard

### *Power BI Case Study Project – Sales Analytics & DAX Implementation*

This repository contains a complete Power BI project analyzing the **sales performance**, **profitability**, and **regional trends** for *AmazingMartEU*, based on a case-study dataset provided for coursework.

The project includes:

* A fully interactive **Power BI Dashboard**
* **Data modeling**, transformations, and relationships
* Custom **DAX measures** and calculated columns
* Dataset description & business questions answered
* Screenshot placeholders for visual representation

---

## 📁 Project Files

| File                           | Description                                                       |
| ------------------------------ | ----------------------------------------------------------------- |
| `AmazingMartEU_Dashboard.pbix` | Main Power BI report file                                         |
| `OowerBI PROJECT.docx`        | Documentation containing case study, questions, DAX, and analysis |
| `README.md`                    | Project overview for GitHub                                       |

---

## 📝 Case Study Overview

You are tasked with building a **Sales Performance Dashboard** for *AmazingMartEU* to help management analyze:

* Total Sales
* Profit & Profit Margin
* Regional Performance
* Customer Segments
* Product Category Trends
* Effect of Discounts on Profitability

The dataset contains two sheets:

### **1. ListOfOrders**

* Order ID
* Order Date, Ship Date
* Customer details
* Region, Country
* Ship Mode

### **2. OrderBreakdown**

* Product Name, Category, Sub-Category
* Sales
* Profit
* Quantity
* Discount

---

## 🛠 Data Preparation & Modeling

Data preparation steps included:

* Loading dataset into Power BI
* Removing errors / missing rows
* Assigning correct data types
* Building relationship on **Order ID**
* Creating calculated columns
* Filtering dataset for relevant years
* Aggregating by Category, Region, Segment

---

## ⚙️ DAX Calculated Columns & Measures

### **Calculated Columns**

```DAX
costprice = OrderBreakdown[Sales] - OrderBreakdown[Profit]

actualprice = OrderBreakdown[Sales] - 
              (OrderBreakdown[Sales] * OrderBreakdown[Discount])
```

### **Key Measures**

```DAX
averagesales = AVERAGE(OrderBreakdown[actualprice])

MAX_ORDERS = MAX(ListOfOrders[Country])
MIN_ORDERS = MIN(ListOfOrders[Country])

maxdelivery_dates = MAX(ListOfOrders[DELIVERY DURATION])
```

---

## 📸 Dashboard Preview 

### **1. Sales Overview Dashboard**

<img width="917" height="537" alt="image" src="https://github.com/user-attachments/assets/12f125ff-9579-4c30-b3e6-db6428066d1c" />

### **2. Profitability Dashboard**

<img width="917" height="458" alt="image" src="https://github.com/user-attachments/assets/70fddb82-4af8-4b6d-aaa7-929b3ede8493" />

### **3. Regional Sales Map**

<img width="917" height="573" alt="image" src="https://github.com/user-attachments/assets/c0e40859-8a19-4ea7-8ac5-7dd725ddab90" />

### **4. Category-Level Performance**

<img width="917" height="538" alt="image" src="https://github.com/user-attachments/assets/ce813062-397c-4c89-9150-d7dc23fc4c33" />

*(Create an `/images` folder in your repo and upload screenshots here.)*

---

## ❓ Key Questions Answered

### **1. What is the average profit margin across all products?**

Calculated by comparing **Total Profit vs Total Sales** to understand overall profitability.

### **2. Which product categories drive the highest total sales?**

Furniture & Office Supplies contribute significantly to revenue.

### **3. What is the distribution of sales by shipping mode?**

Most orders use **Economy** shipping.

### **4. How do discounts affect profitability?**

Higher discounts lower profit — especially in low-margin categories.

### **5. Which regions and countries perform best?**

Regions like **North** and **Central Europe** generate the most revenue.

---

## 🚀 How to Use This Project

1. Download `.pbix` file
2. Open in **Power BI Desktop**
3. Review model, DAX, and visuals
4. Modify or extend the dashboard as needed

---

## 🧑‍💻 Author

**Ayush Ranta**

---

## ⭐ Contributions

Pull requests are welcome!
If you want improvements or new features, feel free to open an issue.

---

## 📄 License

This project is for **educational and academic** use.
