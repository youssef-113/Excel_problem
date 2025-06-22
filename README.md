# 🧹 Excel Column-to-Table Data Cleaner

This project solves a common data cleaning problem where **all records are stored in a single column** of an Excel file, without consistent delimiters or structure. The goal is to transform this messy data into a clean tabular format with rows and columns representing each individual record.

---

## 📁 Input

- A single-column Excel file (`.xlsx`) where:
  - Each group of rows represents one logical record (e.g., a person).
  - There’s no fixed pattern between records.
  - Some rows are irrelevant UI text or contain mixed information (e.g. name, status, rating, language, etc.).

---

## ✅ Output

- A clean Excel file (`processed_output.xlsx`) with the following structure:
  | Status | Name | Rating_Lang | Rating_Value | LastActive | Language1 | Proficiency1 | Language2 | Proficiency2 | ... |
  |--------|------|-------------|---------------|------------|-----------|---------------|-----------|---------------|-----|

- A second Excel file (`unknown_tokens.xlsx`) listing all values that could not be auto-categorized, so you can inspect and improve the classifier.

---

## 🚀 How It Works

1. **Pattern Detection**:
   - Detects record boundaries based on known `status` keywords.
2. **Record Classification**:
   - Identifies fields like:
     - Status
     - Name
     - Rating (e.g., "English • 78")
     - Last active time (e.g., "2 months ago")
     - Languages and their proficiency levels
3. **Unknown Value Reporting**:
   - Any word or phrase that doesn't match known patterns is logged for review.

---
## Link Notebooks
 - on Kaggle [https://www.kaggle.com/code/youssefbassiouny/excel-problem]
 - on Colab [https://colab.research.google.com/drive/1OSmUGgFQM096xeG0yKsvNA75lhgmzV89?usp=sharing]
  
