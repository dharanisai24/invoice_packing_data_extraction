# 📄 Document Data Extraction System

## 🚀 Overview
The Document Data Extraction System is a Python-based application that automatically extracts structured information from business documents such as **Invoices** and **Packing Lists**. The system uses **Tesseract OCR** and Python-based text processing to convert unstructured document content into structured **JSON output**.

## 🎯 Objective
Manual document processing is often time-consuming, error-prone, and inefficient. This project automates the extraction of important data fields to improve speed, accuracy, and consistency.

## ✨ Features
- OCR-based text extraction  
- Document type detection  
- Vendor / key field extraction  
- Line item identification  
- Structured JSON output  

## 🛠 Technologies Used
- Python  
- Tesseract OCR  
- Regex / Text Processing  
- JSON  

## ⚙️ Installation
Install **Tesseract OCR** if not already installed:  
https://github.com/UB-Mannheim/tesseract/wiki

If required, update Tesseract path in code:

```python
pytesseract.pytesseract.tesseract_cmd = r"C:\Program Files\Tesseract-OCR\tesseract.exe"
```

## ▶️ How to Run
```bash
python -m app.main
```
*(or `python main.py` depending on project structure)*

## 🔍 How Data is Extracted
1. The system accepts an invoice or packing list image  
2. Tesseract OCR extracts raw text from the document  
3. Python/OpenCV preprocess the extracted text  
4. Regex/rules detect important fields:
   - Document Type  
   - Vendor Name  
   - Invoice Date  
   - Line Items  
5. Extracted data is converted into structured JSON  

## 📦 Example Output
```json
{
  "Document Type": "Invoice",
  "Vendor Name": "FIDELIS LOGISTICS LIMITED",
  "Invoice Date": "2026-01-19",
  "Line Items": [
    "Handling Charges",
    "Documentation Charges",
    "Seal Charges"
  ]
}
```
## 🔮 Future Enhancements
- PDF document support  
- Web interface (Flask / Streamlit)  
- AI-based classification  
- Database integration  

## 👩‍💻 Author
**SAI DHARANI**

## 📜 License
This project is developed for educational / internship purposes.
