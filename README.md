# Logic Forge – Hackathon Report

**Date:** 14 March 2026

## Project Title

**Chihuahua vs Muffin Classification Using 3LC AI Platform**

---

# 👥 Team Members

* **Karthik Shetty** – Team Lead
* **Anish A**
* **Mithun R Naik**
* **Prajwal P S**

---

# 🎯 Objective

To build a robust **image classification model** that can distinguish between **Chihuahua and Muffin images** using the **3LC AI Platform**, while improving **validation accuracy** by cleaning and relabeling the dataset.

---

# 🛠 Tools & Environment

* **Python:** 3.9
* **Environment:** `3lc-env` virtual environment
* **Platform:** 3LC AI Platform (Dashboard & Service)
* **Framework:** PyTorch
* **Hardware:** CPU / GPU (if available)
* **Dataset:** Chihuahua vs Muffin (Train + Validation images)

---

# 🚀 Step 1: Set Up 3LC Environment

### 1. Create 3LC Account

Obtain API Key from 3LC platform.

### 2. Activate Virtual Environment

```bash
3lc-env\Scripts\activate
```

### 3. Login to 3LC

```bash
3lc login <API_KEY>
```

### 4. Start 3LC Service

```bash
3lc service
```

### 5. Open Dashboard

```
https://dashboard.3lc.ai
```

---

# 📂 Step 2: Start a New Project

Create a new project inside the dashboard.

**Project Name**

```
Chihuahua-Muffin-Fresh
```

Creating a new project helps maintain a **clean workspace without messy or old tables**.

---

# 🤖 Step 3: Initial Training

Run the training script:

```bash
python train.py
```

### Initial Results

* **Model:** ResNet-18 (random initialization)
* **Validation Accuracy:** ~76%
* **Note:** Pretrained weights were not used due to competition rules.

---

# 🔍 Step 4: Inspect & Relabel "Undefined" Images

1. Open **Train Table → 3D Embeddings View** in the Dashboard.
2. Identify clusters labeled **undefined**.
3. Bulk relabel images where classification is obvious:

   * Chihuahua
   * Muffin
4. Leave **ambiguous images** as `undefined`.

⚠️ This step significantly improves model accuracy.

---

# 🔁 Step 5: Retraining After Relabeling

Run the training script again:

```bash
python train.py
```

Results:

* Updated tables reflected **cleaned and relabeled data**.
* **Validation accuracy improved** after dataset cleaning.

---

# ⚠️ Step 6: Challenges & Solutions

| Challenge                                 | Solution                                                       |
| ----------------------------------------- | -------------------------------------------------------------- |
| Old tables messy and unclickable          | Created a **new project** instead of deleting old tables       |
| Many undefined images confusing the model | Used **3D embeddings clustering** to relabel confident samples |
| Limited time for dataset cleaning         | Focused only on **high-confidence relabeling**                 |

---

# 💡 Step 7: Key Learnings

* Always train in a **new project** for a clean workspace.
* Use **3D Embeddings View** to identify clusters for bulk relabeling.
* Only relabel **high-confidence images**.
* Leave ambiguous images as **undefined**.
* Avoid rerunning training multiple times without cleaning tables.

---

# 🏆 Step 8: Outcome

* Built a **clean dataset workflow using 3LC**.
* Improved **validation accuracy through dataset relabeling**.
* Learned **efficient bulk relabeling using 3LC Dashboard**.
* Gained experience with **AI model debugging in competitions**.

---

# 📌 Summary

This project demonstrates how **dataset cleaning and relabeling can significantly improve model performance**, even when using simple architectures like **ResNet-18**.
Using **3LC's visualization tools**, we efficiently identified mislabeled data and improved model accuracy within a limited hackathon timeframe.

---
