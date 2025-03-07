# **Target Encoding Guide**

## **Introduction**
Target encoding is a technique used in Machine Learning (ML) to convert categorical data into numerical values based on the mean (or other statistics) of the target variable. It is commonly used in regression and classification problems when dealing with categorical features with a high number of unique values. 

However, it can introduce data leakage if not applied correctly, making it essential to handle with care. 

---

## **When to Use Target Encoding**
- Suitable for **high-cardinality categorical features** (e.g., city names, product IDs).  
- Works well with **tree-based models** like Decision Trees, Random Forest, and Gradient Boosting.  
- Can improve performance compared to One-Hot Encoding in certain cases.  

- Avoid using it when there are **very few samples per category**, as it may introduce bias.  
- Not ideal for **datasets prone to overfitting**, as it can create data leakage.  

---

## **How Target Encoding Works**
Target Encoding replaces each categorical value with the **mean of the target variable** for that category.  

### **Example: Encoding City Based on House Prices**
| City          | Price |
|--------------|------|
| New York     | 500  |
| Los Angeles  | 450  |
| Chicago      | 400  |
| New York     | 550  |
| Los Angeles  | 480  |

#### **Step 1: Compute Mean Price per City**
| City         | Mean Price |
|-------------|-----------|
| New York    | (500 + 550) / 2 = **525**  |
| Los Angeles | (450 + 480) / 2 = **465**  |
| Chicago     | 400 / 1 = **400** |

#### **Step 2: Replace Categories with Mean Values**
| City          | Price | Encoded City |
|--------------|------|-------------|
| New York     | 500  | **525**  |
| Los Angeles  | 450  | **465**  |
| Chicago      | 400  | **400**  |
| New York     | 550  | **525**  |
| Los Angeles  | 480  | **465**  |

---

## **Avoiding Overfitting in Target Encoding**
One common issue with Target Encoding is **overfitting**, especially when some categories have very few samples. To mitigate this, we use a **smoothing formula** that blends the category mean with the overall target mean.

### **Smoothing Formula**
```math
TE = \frac{n_{cat} \times mean_{cat} + k \times mean_{global}}{n_{cat} + k}
```


### Where:

- mean_cat: The mean of the target variable for a given category.
- mean_global: The overall mean of the target variable in the dataset.
- n_cat: The number of samples in the category.
- k: A smoothing factor that controls how much we rely on the global mean.

### Why Use This Formula?
If a category has a large number of samples (high n_cat), its target mean dominates.
If a category has few samples (low n_cat), the encoding is pulled toward the global mean, reducing overfitting.
The smoothing factor k controls how aggressively the adjustment happens. A higher value makes the encoding more dependent on the global mean.

Note: The smoothing formula applied in target encoding can vary between different libraries.
It is advisable to consult the documentation of the specific library being used to understand its implementation details.

---

## **Python Implementation**
For a full Python implementation, check the Jupyter Notebook **target_encoding.ipynb**. It contains:  
1. A simple example using a small dataset.  
2. A real-world dataset example using **sample_data.csv**.  


## **Pros & Cons**
### Advantages:
- Works well with high-cardinality categorical variables.
- Reduces dimensionality compared to One-Hot Encoding.
- Often improves model performance in regression/classification tasks.

### Disadvantages:
- Risk of Data Leakage – If applied before splitting the dataset, it can introduce bias.
- Overfitting – Can lead to overfitting if categories have too few samples.
- Not ideal for nominal data where categories have no meaningful relationship to the target variable.

## File Structure
This encoding method is part of the ML-Encoding-Guide repository, structured as follows:

```bash
ML-Encoding-Guide/
│── target_encoding/
│   │── target_encoding.md      # Documentation
│   │── target_encoding.ipynb   # Jupyter Notebook example
│   │── sample_data.csv         # Sample dataset
```