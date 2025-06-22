# Mifos Summer of Code 2025 — Phase II: Bank Statement Analysis & Real-Time Insights  

![Banner](https://github.com/user-attachments/assets/d5ee3125-9512-4877-878d-dff3db0b86b1) 

[![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen?style=for-the-badge)](https://github.com/PRIYANSHU2026/Bank-Statement-Analysis-Phase-2)
[![Made with Python](https://img.shields.io/badge/Made%20with-Python-blue?style=for-the-badge)](https://python.org)
[![Mifos Summer of Code 2025](https://img.shields.io/badge/Mifos%20Summer%20of%20Code-2025-blueviolet?style=for-the-badge)](https://mifos.io)
[![AI MultiDomain](https://img.shields.io/badge/AI-MultiDomain-red?style=for-the-badge)](https://github.com/PRIYANSHU2026/Bank-Statement-Analysis-Phase-2)

[![Repo Size](https://img.shields.io/github/repo-size/PRIYANSHU2026/Bank-Statement-Analysis-Phase-2?style=for-the-badge&color=orange)]()
[![Stars](https://img.shields.io/github/stars/PRIYANSHU2026/Bank-Statement-Analysis-Phase-2?style=for-the-badge&color=yellow)](https://github.com/PRIYANSHU2026/Bank-Statement-Analysis-Phase-2)
[![Forks](https://img.shields.io/github/forks/PRIYANSHU2026/Bank-Statement-Analysis-Phase-2?style=for-the-badge&color=purple)](https://github.com/PRIYANSHU2026/Bank-Statement-Analysis-Phase-2)
[![Issues](https://img.shields.io/github/issues/PRIYANSHU2026/Bank-Statement-Analysis-Phase-2?style=for-the-badge&color=teal)](https://github.com/PRIYANSHU2026/Bank-Statement-Analysis-Phase-2/issues)

The **AI-Driven Financial Wellness Platform** represents a significant advancement in personal financial analytics by integrating machine learning, natural language processing (NLP), and real-time dashboards into a unified system for analyzing bank statements and generating adaptive budgeting strategies. This project was developed under the **Mifos Summer of Code 2025** initiative with the goal of empowering users to make informed financial decisions through intelligent insights derived from their transactional data.

Built using **Python, Flask, PostgreSQL, Streamlit, and Plotly**, the platform supports secure access to user-permissioned financial data via **Open Banking APIs (FDX, Akoya)** and offers robust parsing capabilities for **PDF bank statements** using tools like **PyMuPDF, Camelot, and Tesseract OCR**. The system's core innovation lies in its ability to process unstructured financial data, extract meaningful behavioral patterns, detect anomalies, and deliver personalized recommendations tailored to each user’s financial health profile.

---

## 🔍 Project Overview 

This comprehensive platform is designed to unify multi-source transactional data—including bank accounts, investment portfolios, and payment processors—into a single analytical interface. It leverages **machine learning algorithms**, **NLP-based categorization**, and **interactive visualizations** to provide real-time insights into spending habits, savings potential, and debt management strategies.

The platform operates on a modular architecture that includes:

- **Data ingestion layer**: Handles raw inputs from PDFs or Open Banking APIs.
- **ETL pipeline**: Transforms and cleanses data for further analysis.
- **Machine learning engine**: Applies predictive and clustering models to generate actionable intelligence.
- **Recommendation engine**: Provides customized guidance based on user behavior and financial goals.
- **Dashboard interface**: Offers an intuitive, interactive view of financial health metrics and trends.

All code is open-sourced under the **Apache 2.0 License** and hosted by [Mifos Initiative](https://mifos.org),  ensuring transparency, community contribution, and continuous improvement.

---

## ⚙️ Technical Stack

| Layer         | Technology                     |
|---------------|--------------------------------|
| Backend       | Python, Flask                  |
| Database      | PostgreSQL                     |
| ML            | XGBoost, CatBoost, spaCy, NLTK |
| Dashboard     | Streamlit + Plotly             |
| PDF Parsing   | PyMuPDF, Camelot, Tesseract OCR|
| Cloud         | AWS S3, EC2, Textract          |
| APIs          | FDX, Akoya Open Banking        |

---

## 🧠 Key Algorithms & Formulas

At the heart of the platform are several advanced machine learning and statistical models that drive the analytics engine. Each model is selected for its specific use case and optimized for high accuracy and interpretability.

<details>
<summary>✅ 1. Data Preprocessing Pipeline</summary>

### a) Transaction Classification (Hybrid NLP + Regex)

Each transaction description is analyzed to determine its category. A hybrid approach combining NLP-based Named Entity Recognition (NER) and regular expression matching is employed:

```python
def classify_transaction(description):
    description = description.lower()
    if re.search(r"restaurant|cafe|food", description):
        return "Dining"
    elif ner_model(description).label_ == "INVESTMENT":
        return "Investments"
    else:
        return "Other"
