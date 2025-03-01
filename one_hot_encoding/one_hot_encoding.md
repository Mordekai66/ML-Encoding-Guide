# One-Hot Encoding Guide  

## Introduction  
One-Hot Encoding is a technique used in **Machine Learning (ML)** to convert categorical data into a binary matrix representation. It is commonly used for **nominal** categorical data where no inherent order exists among the categories. This method helps models avoid the numerical bias introduced by label encoding.  

---  

## When to Use One-Hot Encoding  
✔ Suitable for **nominal data** (e.g., colors, cities, brands).  
✔ Works well with **linear models** like Linear Regression and Logistic Regression.  
✔ Ideal when categories **do not have a meaningful order**.  

❌ **Avoid using it** when dealing with **high-cardinality features** (features with too many unique categories), as it may increase dimensionality significantly.  

---  

## How One-Hot Encoding Works  
One-Hot Encoding creates **binary columns** for each unique category in a feature. Example:  

| Category | Apple | Banana | Orange |  
|----------|-------|--------|--------|  
| Apple    | 1     | 0      | 0      |  
| Banana   | 0     | 1      | 0      |  
| Orange   | 0     | 0      | 1      |  

Each category is transformed into its own column with a binary value (`1` if present, `0` otherwise).  

---  

## Python Implementation  
For a full Python implementation, check the Jupyter Notebook [`one_hot_encoding.ipynb`](./one_hot_encoding.ipynb). It contains:  
- A **simple example** using a small dataset.  
- A **real-world dataset** example using `sample_data.csv`.  

---  

## Pros & Cons  
### Advantages:  
✔ Eliminates numerical relationships between categories.  
✔ Works well with **nominal categorical features**.  
✔ Compatible with **most ML models**, especially linear ones.  

### Disadvantages:  
❌ Can lead to **high-dimensionality** if there are too many unique categories.  
❌ May increase **memory usage** and slow down training.  

---  

## File Structure  
This encoding method is part of the **ML-Encoding-Guide** repository, structured as follows:  

```bash
ML-Encoding-Guide/
│── one_hot_encoding/
│   │── one_hot_encoding.md      # Documentation
│   │── one_hot_encoding.ipynb   # Jupyter Notebook example
│   │── sample_data.csv          # Sample dataset
