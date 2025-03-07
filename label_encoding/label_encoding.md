# Label Encoding Guide

##  Introduction  
Label Encoding is a technique used in **Machine Learning (ML)** to convert categorical data into numerical values. It is widely used for converting **ordinal** categorical data into a machine-readable format. However, it may introduce issues in models that assume numerical relationships between categories.

---

##  When to Use Label Encoding  
✔ Suitable for **ordinal data** (e.g., Low < Medium < High).  
✔ Works well with **tree-based algorithms** like Decision Trees and Random Forest.  
✔ Useful when there are **few unique categories** in the dataset.

❌ **Avoid using it** with algorithms that assume numerical relationships (e.g., Linear Regression), as it may introduce unintended bias.

---

##  How Label Encoding Works  
Label Encoding assigns a unique integer to each category in a feature. Example:

| Category | Encoded Value |
|----------|--------------|
| Apple    | 0            |
| Banana   | 1            |
| Orange   | 2            |

This numerical representation allows ML models to process categorical data efficiently.

---

##  Python Implementation  
For a full Python implementation, check the Jupyter Notebook [`label_encoding.ipynb`](./label_encoding.ipynb). It contains:
- A **simple example** using a small dataset.
- A **real-world dataset** example using [`sample_data.csv`](./sample_data.csv).

---

##  Pros & Cons  
###  Advantages:  
✔ Simple and efficient.  
✔ Suitable for **ordinal categorical features**.  
✔ Compatible with **tree-based models**.  

###  Disadvantages:  
❌ Can introduce **misleading relationships** in models that assume numerical order.  
❌ **Not ideal for nominal data** (e.g., colors, cities, names).  

---

##  File Structure  
This encoding method is part of the **ML-Encoding-Guide** repository, structured as follows:

```bash
ML-Encoding-Guide/
│── label_encoding/
│   │── label_encoding.md      # Documentation
│   │── label_encoding.ipynb   # Jupyter Notebook example
│   │── sample_data.csv        # Sample dataset
