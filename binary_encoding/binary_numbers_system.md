# **Binary Number System**

## **Introduction**

The **binary number system**, also known as the **base-2 system**, is a numerical system that represents values using only two digits: **0 and 1**. It is the foundation of all modern computing systems and digital electronics.  
[Read more on Wikipedia](https://en.wikipedia.org/wiki/Binary_number).

---

## **Structure and Representation**

Each digit in a binary number represents a power of **2**, starting from **2⁰** on the right.  

For example, the binary number **1011** is calculated as follows:

- **1 × 2³ = 8**
- **0 × 2² = 0**
- **1 × 2¹ = 2**
- **1 × 2⁰ = 1**

Thus, **1011 (binary) = 11 (decimal)**.

---

## **Uses of the Binary System**

The binary system is essential in:

- **Computers**: Data and instructions are represented in binary form.
- **Digital circuits**: Electrical signals operate with ON (1) and OFF (0) states.
- **Networking and storage**: Binary encodes everything from images to sound.
- **Boolean logic**: Logical operations (AND, OR, NOT) use binary values.
- **Cryptography**: Secure communication relies on binary-based encryption.

---

## **Binary Arithmetic Operations**

Binary arithmetic follows simple rules similar to the decimal system but only involves 0s and 1s.

### **Binary Addition Rules:**
- **0 + 0 = 0**
- **0 + 1 = 1**
- **1 + 0 = 1**
- **1 + 1 = 10** (carry 1 to the next column)

#### **Example: Adding Two Binary Numbers**
```
  1011
+ 1101
------
 11000
```

### **Binary Subtraction Rules:**
- **0 - 0 = 0**
- **1 - 0 = 1**
- **1 - 1 = 0**
- **0 - 1 = 1** (borrow 1 from the left)

#### **Example: Subtracting Two Binary Numbers**
```
  1011
-  0110
------
  0101
```

### **Binary Multiplication Rules:**
- **0 × 0 = 0**
- **0 × 1 = 0**
- **1 × 0 = 0**
- **1 × 1 = 1**

#### **Example: Multiplying Two Binary Numbers**
```
   101
×   11
------
   101
+ 1010
------
  1111
```

### **Binary Division Rules:**
Binary division works like long division in the decimal system but only uses 0s and 1s.

#### **Example: Dividing Two Binary Numbers**
```
 1010 ÷ 10 = 101
```

---

## **Converting Between Number Systems**

### **Decimal to Binary Conversion**
To convert a decimal number to binary, follow these steps:

1. **Divide the number by 2**.
2. **Write down the remainder**.
3. **Repeat the process with the quotient** until it reaches 0.
4. **Read the binary digits from bottom to top**.

#### **Example: Converting 13 (decimal) to Binary**
- 13 ÷ 2 = 6 **remainder 1**
- 6 ÷ 2 = 3 **remainder 0**
- 3 ÷ 2 = 1 **remainder 1**
- 1 ÷ 2 = 0 **remainder 1**

So, **13 (decimal) = 1101 (binary)**.

### **Binary to Decimal Conversion**
To convert a binary number to decimal, multiply each bit by its power of 2 and sum the values.

#### **Example: Converting 1101 (binary) to Decimal**
- **1 × 2³ = 8**
- **1 × 2² = 4**
- **0 × 2¹ = 0**
- **1 × 2⁰ = 1**

Total: **8 + 4 + 0 + 1 = 13 (decimal)**.

### **Binary to Hexadecimal Conversion**
Each **4-bit** binary sequence corresponds to a single **hexadecimal digit (0-9, A-F)**.

#### **Example: Converting 11010110 (binary) to Hexadecimal**
1. Split into 4-bit groups: **1101 0110**
2. Convert each group:
   - **1101 (D)**
   - **0110 (6)**

So, **11010110 (binary) = D6 (hexadecimal)**.

### **Hexadecimal to Binary Conversion**
Convert each hex digit to a **4-bit** binary representation.

#### **Example: Converting A9 (hex) to Binary**
- **A = 1010**
- **9 = 1001**

So, **A9 (hex) = 10101001 (binary)**.

---

## **Binary Logic and Boolean Algebra**

Binary values follow Boolean algebra, used in logic gates and circuit design.

### **Common Boolean Operations**
| Operation | Symbol | Truth Table |
|-----------|--------|------------|
| AND       | ∧      | 1 if both are 1 |
| OR        | ∨      | 1 if at least one is 1 |
| NOT       | ¬      | Flips 0 to 1 and 1 to 0 |
| XOR       | ⊕      | 1 if inputs are different |

#### **Example: AND Gate**
| A | B | A ∧ B |
|---|---|-------|
| 0 | 0 | 0     |
| 0 | 1 | 0     |
| 1 | 0 | 0     |
| 1 | 1 | 1     |

---

## **Real-World Applications of Binary Numbers**

1. **Computers & Digital Systems**:
   - Processors, memory, and storage all use binary.
   - Data is stored in bits (0s and 1s).
   
2. **Networking**:
   - IP addresses (e.g., `192.168.1.1`) are converted to binary.

3. **Cryptography**:
   - Binary encoding helps secure data transmission.

4. **Image and Sound Processing**:
   - Images use **binary pixel values (black = 0, white = 1)**.
   - Audio files store sound waves digitally using binary.

5. **Machine Learning & AI**:
   - Binary encoding is used in feature engineering for categorical data.

---

## **References**
- [Wikipedia - Binary Number](https://en.wikipedia.org/wiki/Binary_number)
- [Boolean Algebra - Wikipedia](https://en.wikipedia.org/wiki/Boolean_algebra)
- [Number Systems in Computing](https://en.wikipedia.org/wiki/Numeral_system)
