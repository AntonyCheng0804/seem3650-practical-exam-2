BabyGPT Mini Project

**Student ID:** 1155193432  
**Course:** SEEM3650  

---

## 📌 Project Description

This project explores the training of a miniaturized GPT model (BabyGPT) using [nanoGPT](https://github.com/karpathy/nanoGPT). The project is divided into three main parts:

1. **Training on Shakespeare text** to learn basic language modeling.
2. **Architecture exploration** by varying attention heads while keeping layers fixed.
3. **Training on custom C/C++ code** to explore BabyGPT's ability to learn programming patterns.

---

## 🧪 What’s Included

| File/Folder                         | Description |
|------------------------------------|-------------|
| `report.md`                        | Final report documenting results, losses, samples, and analysis |
| `figures/loss_vs_heads.png`        | Plot showing validation loss vs number of heads |
| `config/train_code_generation.py`  | Config file used for training BabyGPT on C/C++ code |
| `data/code_generation/input.txt`   | Dataset file containing C/C++ code |


---

## 🚀 How to Run

> The project was completed entirely in **Google Colab**, using nanoGPT.

### 1. Clone the repository
```bash
git clone https://github.com/AntonyCheng0804/seem3650-practical-exam-2.git
cd seem3650-practical-exam-2
