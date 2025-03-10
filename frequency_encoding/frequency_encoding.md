# **Frequency Encoding Guide**

## **Introduction**
Frequency encoding is a technique used in Machine Learning (ML) to convert categorical data into numerical values based on the frequency of each category in the dataset. It is particularly useful when dealing with high-cardinality categorical features and helps simplify data representation without increasing dimensionality, unlike One-Hot Encoding.

However, if not applied correctly, it can introduce biases, making it essential to handle with care.

---

## **When to Use Frequency Encoding**
- Suitable for **high-cardinality categorical features** (e.g., city names, product IDs).  
- Works well with **tree-based models** like Decision Trees, Random Forest, and Gradient Boosting.  
- Helps reduce dimensionality compared to One-Hot Encoding.  

**Avoid using it when:**  
- The frequency of a category does not correlate with the target variable, as it may add noise.  
- The dataset has **uniform category distributions**, as it may not provide useful differentiation.

---

## **How Frequency Encoding Works**
Frequency Encoding replaces each categorical value with the **count of times** that category appears in the dataset.

### **Example: Encoding City Based on Frequency (Without Normalization)**

#### **Original Data:**
| City          | Price |
|--------------|------|
| New York     | 500  |
| Los Angeles  | 450  |
| Chicago      | 400  |
| New York     | 550  |
| Los Angeles  | 480  |

#### **Step 1: Compute Frequency of Each City**
| City         | Frequency |
|-------------|-----------|
| New York    | 2  |
| Los Angeles | 2  |
| Chicago     | 1  |

#### **Step 2: Replace Categories with Frequency Values**
| City          | Price | Encoded City |
|--------------|------|-------------|
| New York     | 500  | **2**  |
| Los Angeles  | 450  | **2**  |
| Chicago      | 400  | **1**  |
| New York     | 550  | **2**  |
| Los Angeles  | 480  | **2**  |

---

## **Avoiding Pitfalls in Frequency Encoding**
One common issue with Frequency Encoding is **introducing unintended correlations**, especially when the frequency of a category is strongly related to the target variable in an unintended way. To mitigate this:

- **Normalize Frequencies**: Convert counts into proportions relative to the dataset size.  
- **Apply Log Transformation**: If frequency values vary significantly, applying a log transformation can help reduce the impact of dominant categories.  
- **Use Binning**: If some categories have very low frequencies, grouping them into an "Other" category can improve model stability.

### **Example: Encoding City Based on Normalized Frequency**

#### **Step 1: Compute Normalized Frequency of Each City**
| City         | Normalized Frequency |
|-------------|----------------------|
| New York    | 2/5 = **0.4**  |
| Los Angeles | 2/5 = **0.4**  |
| Chicago     | 1/5 = **0.2**  |

#### **Step 2: Replace Categories with Normalized Frequency Values**
| City          | Price | Encoded City (Normalized) |
|--------------|------|--------------------------|
| New York     | 500  | **0.4**  |
| Los Angeles  | 450  | **0.4**  |
| Chicago      | 400  | **0.2**  |
| New York     | 550  | **0.4**  |
| Los Angeles  | 480  | **0.4**  |

---

## **Python Implementation**
For a full Python implementation, check the Jupyter Notebook [`frequency_encoding.ipynb`](./frequency_encoding.ipynb). It contains:  
1. A simple example using a small dataset.  
2. A real-world dataset example using [`sample_data.csv`](./sample_data.csv).  

---

## **Pros & Cons**
### **Advantages:**
- Works well with high-cardinality categorical variables.  
- Reduces dimensionality compared to One-Hot Encoding.  
- Retains useful information about category distribution.  

### **Disadvantages:**
- May introduce bias if frequency correlates strongly with the target variable.  
- Less effective for datasets where category frequency does not hold predictive value.  
- Not ideal for nominal data where categories have no meaningful relationship.

## **File Structure**
This encoding method is part of the ML-Encoding-Guide repository, structured as follows:

```bash
ML-Encoding-Guide/
│── frequency_encoding/
│   │── frequency_encoding.md      # Documentation
│   │── frequency_encoding.ipynb   # Jupyter Notebook example
│   │── sample_data.csv            # Sample dataset
```

