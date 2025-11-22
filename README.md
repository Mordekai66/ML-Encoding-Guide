# ML Encoding Guide  
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Guide-orange)
![Encoding](https://img.shields.io/badge/Encoding-Techniques-success)
![Scikit-learn](https://img.shields.io/badge/Scikit--Learn-Label%20Encoding%20%7C%20OneHot-red)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Processing-green)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-yellow)
![License](https://img.shields.io/badge/License-MIT-green)
![Education](https://img.shields.io/badge/Education-Tutorial-purple)

## Introduction  
Most Machine Learning (ML) models work with numerical data, but real-world datasets often contain categorical features (e.g., countries, product categories, user types). Encoding these features properly can dramatically impact model performance. This repository provides a **detailed guide** to the most commonly used encoding techniques, explains when to use each one, and includes **Python implementations** for practical applications.  

---

## Covered Encoding Techniques  

This repository provides a **detailed breakdown** of the most widely used feature encoding techniques in Machine Learning. Each encoding method includes:

✔ **When to Use It** – The best scenarios for each encoding technique.  
✔ **How It Works** – A step-by-step explanation of the transformation.  
✔ **Python Implementation** – Hands-on examples with code.  
✔ **Practical Application** – Real-world datasets to illustrate usage.  

The following encoding methods are included:  

- **Label Encoding**  
- **One-Hot Encoding**  
- **Target Encoding**  
- **Frequency Encoding**  
- **Binary Encoding**  

Each technique is implemented in **Jupyter Notebooks** with accompanying datasets to enhance learning.

---

## Encoding Techniques Comparison  

| Encoding Type | Pros | Cons | Best Used For |
|--------------|------|------|--------------|
| **Label Encoding** | Simple, fast | May introduce unintended ordinal relationships | Small categorical features |
| **One-Hot Encoding** | No ordinal issues | Can create very large feature spaces | Low-cardinality categorical data |
| **Target Encoding** | Useful for high-cardinality features | Prone to target leakage | Categorical features in supervised learning |
| **Frequency Encoding** | Captures some statistical info | May not work well with all ML models | Features with skewed distributions |
| **Binary Encoding** | Reduces dimensionality | Harder to interpret | High-cardinality categorical features |

---

## Repository Structure  

```bash
ML-Encoding-Guide/
│── label_encoding/            # Label Encoding files
│   │── label_encoding.md      # Documentation for Label Encoding
│   │── label_encoding.ipynb   # Jupyter Notebook example
│   │── sample_data.csv        # Sample dataset
│
│── one_hot_encoding/          # One-Hot Encoding files
│   │── one_hot_encoding.md    # Documentation for One-Hot Encoding
│   │── one_hot_encoding.ipynb # Jupyter Notebook example
│   │── sample_data.csv        # Sample dataset
│
│── target_encoding/           # Target Encoding files
│   │── target_encoding.md     # Documentation for Target Encoding
│   │── target_encoding.ipynb  # Jupyter Notebook example
│   │── sample_data.csv        # Sample dataset
│
│── frequency_encoding/        # Frequency Encoding files
│   │── frequency_encoding.md  # Documentation for Frequency Encoding
│   │── frequency_encoding.ipynb # Jupyter Notebook example
│   │── sample_data.csv        # Sample dataset
│
│── binary_encoding/           # Binary Encoding files
│   │── binary_encoding.md     # Documentation for Binary Encoding
│   │── binary_encoding.ipynb  # Jupyter Notebook example
│   │── binary_numbers_system.md  # binary encoding system explained
│
│── README.md                  # Project documentation
│── LICENSE                     # License file
```

---

## How to Use the Repository  

1. **Clone the repository**  
   ```bash
   git clone https://github.com/Mordekai66/ML-Encoding-Guide.git
   cd ML-Encoding-Guide
   ```
2. **Install dependencies**  
   ```bash
   pip install -r requirements.txt
   ```
3. **Open a Jupyter Notebook**  
   ```bash
   jupyter notebook
   ```
4. **Navigate to the encoding method of your choice and explore the notebooks!**  

---

## License  
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.  

---

## Contribute & Support  
If you find this repository useful, please consider giving it a ⭐! Feel free to submit issues, feature requests, or pull requests.  
