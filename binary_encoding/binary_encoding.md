# **Binary Encoding Guide**

## **Introduction**
Binary Encoding is a technique used in Machine Learning (ML) to convert categorical data into numerical form while reducing dimensionality. It is a hybrid approach combining elements of One-Hot Encoding and Ordinal Encoding. 

Unlike One-Hot Encoding, which creates a separate column for each category, Binary Encoding represents categories using binary digits, significantly reducing the number of columns required.

---

## **When to Use Binary Encoding**
- Suitable for **high-cardinality categorical features** (e.g., product IDs, user IDs).  
- Works well with **tree-based models** and **linear models**.  
- Helps reduce dimensionality compared to One-Hot Encoding.  

**Avoid using it when:**  
- The dataset contains very few categories (One-Hot Encoding might be simpler).  
- Interpretability is crucial since binary representation may be hard to decipher.  

---

## **How Binary Encoding Works**
Binary Encoding involves three main steps:
1. **Convert categories into integer values** using Ordinal Encoding.
2. **Transform these integers into their binary representation.**
3. **Split the binary digits across multiple columns.**

### **Example: Encoding Vehicle Types Using Binary Encoding**

#### **Original Data:**
| Vehicle Type | 
|-------------|
| Car         |
| Bike        |
| Motorbike   |
| Bus         |

#### **Step 1: Convert to Integer Values**
| Vehicle Type | Integer Value |
|-------------|--------------|
| Car         | 1            |
| Bike        | 2            |
| Motorbike   | 3            |
| Bus         | 4            |

#### **Step 2: Convert to Binary Representation**
| Vehicle Type | Integer Value | Binary Code |
|-------------|--------------|-------------|
| Car         | 1            | 01          |
| Bike        | 2            | 10          |
| Motorbike   | 3            | 11          |
| Bus         | 4            | 100         |

#### **Step 3: Split Binary Code into Separate Columns**
| Vehicle Type | Binary Code | Col 1 | Col 2 | Col 3 |
|-------------|------------|-------|-------|-------|
| Car         | 01         | 0     | 1     | -     |
| Bike        | 10         | 1     | 0     | -     |
| Motorbike   | 11         | 1     | 1     | -     |
| Bus         | 100        | 1     | 0     | 0     |

> **Note:** The number of binary columns depends on the highest integer value.
---

## **Want to understand how binary numbers work?**
- Before diving deeper into Binary Encoding, it's important to understand how binary numbers are formed and why they are used. Check out [`binary_numbers.md`](./binary_numbers_system.md) for a quick guide on binary number representation.

---

## **Avoiding Pitfalls in Binary Encoding**
While Binary Encoding is efficient, it has some drawbacks:

- **Loss of Interpretability:** The encoded values do not retain human-readable meanings.
- **Increased Complexity:** Compared to simpler encodings, binary columns might be harder to analyze directly.
- **Potential Information Loss:** Although Binary Encoding reduces dimensionality, some relationship structures within the data may be lost.

### **Solutions:**
- **Combine Binary Encoding with other techniques** (e.g., Target Encoding) for better performance.
- **Ensure that encoded values retain useful information** by validating the model’s performance.
- **Normalize Binary Values** if the model is sensitive to binary distributions.

---

## **Python Implementation**
For a full Python implementation, check the Jupyter Notebook [`binary_encoding.ipynb`](./binary_encoding.ipynb). It contains:  
1. A simple example using a small dataset.  
2. A real-world dataset example using [`sample_data.csv`](./sample_data.csv).  

---

## **Pros & Cons**
### **Advantages:**
✅ Reduces dimensionality compared to One-Hot Encoding.  
✅ Suitable for high-cardinality categorical data.  
✅ Retains some ordinal relationships compared to Ordinal Encoding.  

### **Disadvantages:**
❌ Less interpretable than One-Hot Encoding.  
❌ May lose structural information within categories.  
❌ Can still introduce correlations that might affect model performance.  

---

## **File Structure**
This encoding method is part of the ML-Encoding-Guide repository, structured as follows:
```bash
ML-Encoding-Guide/
│── binary_encoding/
│   │── binary_encoding.md      # Documentation
│   │── binary_encoding.ipynb   # Jupyter Notebook example
│   │── sample_data.csv         # Sample dataset
```
