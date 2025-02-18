# 🏦 **Loan Eligibility Analyzer**

![GitHub License](https://img.shields.io/badge/license-MIT-blue.svg) ![Python Version](https://img.shields.io/badge/python-3.8%20%7C%203.9%20%7C%203.10-blue) ![Groq API](https://img.shields.io/badge/Groq-API-green)

A lightweight and intelligent loan eligibility analyzer that evaluates financial and ESG-related information from uploaded documents (DOCX/PDF) to determine loan eligibility. Built with simplicity in mind, this tool uses Groq's advanced AI models to extract relevant data, calculate scores, and provide user-friendly feedback.

---

## 🌟 **Features**

- **Document Analysis**: Extracts key financial and ESG-related information from DOCX and PDF files.
- **Dynamic Scoring**: Assigns scores based on simplified thresholds for easy evaluation.
- **Relaxed Thresholds**: Ensures fairness by adjusting thresholds dynamically based on missing conditions.
- **User-Friendly Feedback**: Provides constructive feedback for both approved and rejected applications.
- **Powered by Groq**: Utilizes Groq's `qwen-2.5-32b` model for accurate and efficient data extraction.
- **Customizable**: Easily adjust scoring thresholds and conditions to suit your needs.

---

## 🛠️ **How It Works**

1. **Upload Document**: Provide a DOCX or PDF file containing financial and ESG-related information.
2. **Extract Information**: The script uses Groq's AI model to extract relevant data such as CIBIL Score, Annual Income, Bank Balance, etc.
3. **Evaluate Conditions**: Scores are calculated based on relaxed thresholds for each condition.
4. **Determine Eligibility**: If the total score meets or exceeds the adjusted threshold, the user is eligible for a loan.
5. **Provide Feedback**: Clear and friendly feedback is provided for both eligible and rejected users.

---

## 🗈️ **Key Conditions**

The following conditions are evaluated to determine loan eligibility:

| **Condition**                  | **Threshold**           | **Score** |
|--------------------------------|-------------------------|-----------|
| CIBIL Score                    | ≥ 600                  | 1         |
| Annual Income or Turnover      | ≥ ₹300,000             | 1         |
| Bank Balance & Multiple Accounts | ≥ ₹50,000            | 1         |
| Utility Payments (On-Time Ratio) | ≥ 70%                | 1         |
| ESG Related Information        | Optional               | 1         |

---

## 🚀 **Getting Started**

### **Prerequisites**

- Python 3.8 or higher
- Groq API Key (Sign up at [Groq](https://groq.com))
- Install required libraries:
  ```bash
  pip install python-docx pdfplumber groq
  ```

### **Model Download**

Download the pre-trained model (`.pth` file) from Google Drive:
[Loan Eligibility Model - Google Drive](https://drive.google.com/file/d/19ENWebO3RXZCyG1aEFwPafs1sQYdCfer/view?usp=sharing)

### **Installation**

Clone the Repository:
```bash
git clone https://github.com/yourusername/loan-eligibility-analyzer.git
cd loan-eligibility-analyzer
```

### **Set Up Your Groq API Key**

Create a `.env` file in the root directory and add your API key:
```plaintext
GROQ_API_KEY=your_api_key_here
```

### **Run the Script**
```bash
python main.py path/to/your/file.docx
```

### **📂 File Structure**
```bash
loan-eligibility-analyzer/
├── main.py                  # Main script for loan eligibility analysis
├── .env                     # Environment file for storing API keys
├── requirements.txt          # List of required Python libraries
├── README.md                 # This file
└── example_files/            # Example DOCX/PDF files for testing
    ├── sample_loan_doc.docx
    └── sample_loan_doc.pdf
```

---

## 🤦🏻‍♂️ **Example Usage**

Input File: `sample_loan_doc.docx`

```plaintext
CIBIL Score: 650
Annual Income: ₹400,000
Bank Balance: ₹75,000
Utility Payments On-Time Ratio: 80%
ESG Initiatives: 1
```

Output:
```plaintext
Great news! You are eligible for a loan. Our team will contact you soon.
```

---

## 🎯 **Customization**

You can easily customize the scoring system and thresholds by modifying the `CONDITION_THRESHOLDS` dictionary in `main.py`. For example:

```python
CONDITION_THRESHOLDS = {
    "CIBIL Score": {"max_score": 1, "good_threshold": 650},  # Adjusted threshold
    "Annual Income or Turnover": {"max_score": 1, "min_income": 400000},  # Higher income requirement
}
```

---

## 🐝 License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## 👌 Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request if you have ideas for improvements or new features.

---

## 📧 Contact
For questions or feedback, feel free to reach out:

- Email: your.email@example.com
- GitHub: @yourusername

---

## 🌐 Acknowledgments
- Special thanks to Groq for their powerful AI models.
- Inspired by the need for a lightweight and user-friendly loan eligibility analyzer.

---

### Clone the Repository

```bash
git clone https://github.com/yourusername/loan-eligibility-analyzer.git
cd loan-eligibility-analyzer
```

---

### Set Up Your Groq API Key

Create a `.env` file and add the API key:
```plaintext
GROQ_API_KEY=your_api_key_here
```

---

