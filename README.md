# Mishra Prime Estimator

### 📌 Author: Divya Prakash Mishra  
### 🔢 Project: Predicting Prime Numbers with Enhanced Accuracy  

---

## 🧠 Overview

The **Mishra Prime Estimator** is a novel mathematical formula designed to predict the *(n)ᵗʰ prime number* using a blend of logarithmic components, sinusoidal correction, and complex oscillations. It provides high accuracy compared to traditional approximations and opens new directions for prime number analysis—potentially relevant to the **Riemann Hypothesis**.

---

## 🧮 Core Formula

\[
P_n ≈ 1.165·n·\log(n) − 0.18·\log(n) + \frac{n}{4.2·\log(n)} − 0.62·\sin(1.39·n) + \Re\left(0.5·e^{i·n·\pi/4} + 0.35·e^{i·n·\pi/6}\right)
\]

Where:
- \(n\) is the prime index
- \(\Re\) denotes the real part of a complex number
- \(P_n\) is the predicted \(n\)th prime

---

## 📊 Features

- High accuracy for predicting \(P_n\)
- Complex oscillations reflect deeper prime structure
- Error modeling and correction functions included
- Python implementation for direct use

---

## 🐍 Python Implementation

```python
import math
import cmath

def mishra_prime_estimator(n):
    logn = math.log(n)
    term1 = 1.165 * n * logn
    term2 = -0.18 * logn
    term3 = n / (4.2 * logn)
    term4 = -0.62 * math.sin(1.39 * n)
    term5 = cmath.exp(1j * n * math.pi / 4) * 0.5 + cmath.exp(1j * n * math.pi / 6) * 0.35
    return round(term1 + term2 + term3 + term4 + term5.real)
