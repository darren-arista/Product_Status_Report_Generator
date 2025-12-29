# 📊 Automation Projects by Falguni Bhosle  
## Product Published Status Comparison & Summary Report Automation

A Flask-based Excel automation tool that **compares daily product catalogs**, identifies **published, unpublished, hidden, and new products**, and generates a **professionally formatted Excel report** with historical summaries — all in seconds.

---

## 🚀 Project Overview

Manual comparison of daily product catalogs was time-consuming, error-prone, and inconsistent. Operations teams had to:

- Compare today’s and yesterday’s files manually  
- Track hidden products line-by-line  
- Maintain historical summaries in Excel  
- Ensure branding and formatting consistency  

This automation **eliminates manual effort** by generating a **fully formatted Excel report** with summaries, conditional formatting, and branding through a simple web interface.

**Ideal for:**  
E-commerce operations, catalog management, and logistics reporting.

---

## ✨ Key Features

- ✅ Supports **Excel (.xlsx / .xls)** and **CSV** files  
- 🔍 **Intelligent column detection** (case-insensitive, no fixed template needed)  
- 🆕 Detects **new, unpublished, and hidden products**  
- 📈 Auto-generated **historical summary dashboard**  
- 🎨 Conditional formatting, borders, gridlines & column sizing  
- 🖼️ Automatic **logo embedding** (KITH branding with fallback)  
- 🌐 Fully automated via **Flask web interface**  
- 📦 Handles file uploads up to **100MB**

---

## 🛠️ Tech Stack

| Component | Technology |
|--------|------------|
| Backend | Python, Flask |
| Data Processing | Pandas |
| Excel Automation | OpenPyXL |
| Frontend | HTML, Jinja Templates |
| Image Handling | Pillow |

---

## ⚙️ Installation

Follow these steps to run the project locally:

1. Clone the repository
   ```bash
   git clone https://github.com/your-username/product-status-report-automation.git
   cd product-status-report-automation

2. Create & activate a virtual environment (recommended)

python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate # macOS/Linux


3. Install required dependencies

pip install -r requirements.txt


4. Run the Flask application

python app.py


5. Open the app in your browser

http://127.0.0.1:5000/

▶️ Usage Instructions
Step 1: Upload Files

Upload the following through the web UI:

Today’s Product File (mandatory)

Yesterday’s Raw Product File (mandatory)

Yesterday’s Final Report (optional – for historical summary)

Step 2: Automated Processing

Files are read using Pandas

Columns like Handle, Title, Vendor, Product ID, Published are auto-detected

Boolean published status is derived automatically

Step 3: Comparison Logic
Scenario	Result
Published yesterday → Unpublished today	Hidden Product
Product exists today but not yesterday	New Product
Published today	Marked as TRUE
Step 4: Excel Report Generation

📅 Sheet named using business date (e.g., 5th Nov’25)

🎨 Conditional formatting applied

📐 Borders, gridlines & column widths standardized

Step 5: Summary Sheet

The summary sheet includes:

Date

Published products count

Unpublished products count

Hidden products information

Automatically appends historical data

🎨 Conditional Formatting Rules
Condition	Color
Hidden Products	Green
Other Products	Yellow
🔗 API Routes
Route	Method	Description
/	GET	Upload UI
/generate	POST	Generate Excel report
413	ERROR	File size exceeded
📤 Output

📁 Downloadable Excel (.xlsx) file

📊 Daily comparison sheet

📈 Historical Summary sheet

🤝 Contributing (Optional)

Contributions are welcome!

Fork the repository

Create a new branch (feature/your-feature-name)

Commit your changes

Open a Pull Request

📄 License (Optional)

This project is licensed under the MIT License.
You are free to use, modify, and distribute it with attribution.

👩‍💻 Author

Falguni Bhosle
Automation & Logistics Reporting Enthusiast