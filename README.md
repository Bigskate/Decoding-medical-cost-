# 🩺 Decoding Medical Costs: Analyzing Insurance Data with Power BI

### 📘 Project Overview
Healthcare expenses can vary widely based on lifestyle and personal factors — but what truly drives those differences?
This Power BI project explores **medical cost patterns** to understand how **age, BMI, smoking, and region** affect the total charges billed to patients.

The goal is to create an **analytical storytelling dashboard** that visualizes and communicates insights clearly.

---

## 🎯 Problem Statement
Rising healthcare costs are a global concern. Insurers and individuals often lack clarity on how personal habits (like smoking) or metrics (like BMI) influence medical expenses.
This dashboard helps **decode these cost patterns**, empowering better health and financial decisions.

---

## 💡 Objectives
- Visualize the relationship between **demographics** and **medical costs**
- Compare spending between **smokers vs. non-smokers**
- Identify cost patterns across **BMI categories** and **regions**
- Communicate insights through **data storytelling visuals**

---

## 🧮 Dataset
**Dataset name:** Decoding Medical Costs: Analyzing Insurance Data
**Source:** Open data (Kaggle)
**Rows:** 1,338
**Columns:** `age`, `sex`, `bmi`, `children`, `smoker`, `region`, `charges`

---

## 🛠 Tools & Techniques
- **Power BI Desktop** – Visualization & modeling
- **Power Query** – Data cleaning and transformation
- **DAX** – Measures, KPIs, calculated columns
- **Tooltips & Slicers** – Interactive exploration

---

## ⚙️ Key Calculations

**BMI Category (Calculated Column):**
```DAX
BMI Category =
SWITCH(
TRUE(),
Data[BMI] < 18.5, "Underweight",
Data[BMI] >= 18.5 && Data[BMI] < 25, "Normal",
Data[BMI] >= 25 && Data[BMI] < 30, "Overweight",
Data[BMI] >= 30, "Obese"
)
