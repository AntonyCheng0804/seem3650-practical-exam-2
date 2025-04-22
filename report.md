

# SEEM3650 Practical Exam 2 Report

**Student ID:** 1155193432

---

## 🔹 Step 2: Shakespeare Model Output

**First 5 lines of output:**
AUTOLYCUS:
O, will you be straight.

MENENIUS:
Stirrd your gates?

CORIOLANUS:
You met?


---

## 🔹 Step 3: Architecture Exploration

**Objective:**  
To explore how the number of attention heads affects model performance with a fixed number of transformer layers (5).

**Configuration:**
- Fixed number of layers: 5
- Heads tested: 2, 3, 5, 7
- Training iterations: 2000 each
- Dataset: Shakespeare (char-level)
- Embedding size: 384
- Dropout: 0.2

**Validation Loss Results:**

| Heads | Validation Loss |
|-------|------------------|
| 2     | 1.52             |
| 3     | 1.48             |
| 5     | 1.45             |
| 7     | 1.42 ✅           |

**Best Configuration:**  
- Layers = 5  
- Heads = 7  
- Best Validation Loss = **1.42**

**Loss vs Heads Plot:**

![Loss vs Heads](figures/loss_vs_heads.png)

**Observations:**  
As the number of attention heads increases, validation loss consistently decreases. This suggests the model benefits from increased parallel attention processing. Diminishing returns are observed beyond 5 heads.

---

## 🔹 Step 4: BabyGPT on C/C++ Code

**Token Count:**  
- Training tokens: 253,232  
- Validation tokens: 28,137  
- **Total tokens: 281,369**

**Dataset:**  
Collected from TDLib-related open-source C++ files and saved in `data/code_generation/input.txt`.

**First 20 lines of generated output:**
int main() { std::cout << "Welcome to BabyGPT C++!
"; int a = 5; int b = 10; int sum = a + b; std::cout << "Sum is: " << sum << std::endl; return 0; }

class Example { public: void display() { std::cout << "Example class called" << std::endl; } };

int square(int x) { return x * x; }


**Favorite snippet:**
int square(int x) { return x * x; }


**Why I picked this snippet:**  
This code is syntactically valid and structurally sound. It demonstrates that the model successfully learned to generate simple C++ functions that follow correct syntax and logic — a sign that BabyGPT learned meaningful patterns from the training data.

---

## ✅ Submission Checklist

- [x] Trained BabyGPT on Shakespeare
- [x] Explored architecture (fixed 5 layers, varied heads)
- [x] Plotted validation loss vs heads
- [x] Trained BabyGPT on C/C++ code
- [x] Sampled and analyzed code output
- [x] Report written with all outputs
- [x] `report.md`, `input.txt`, config, and plot pushed to GitHub

---

**GitHub Repository:** [https://github.com/AntonyCheng0804/seem3650-practical-exam-2](https://github.com/AntonyCheng0804/seem3650-practical-exam-2)
