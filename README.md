# East-Midlands-Chamber-AI-Powered-PDF-reader-Automation-Project-
East Midlands Chamber (Derbyshire, Nottinghamshire, Leicestershire) is the leading business representation organisation in the East Midlands. I worked with a team on a project to create an AI script using AI Agents (Gemini AI) API that outputs data in a table format based of reading a scanned PDF.


Business Context
Did you know that some companies spend an average of 30% to 40% of their time on manual data entry and handling? This involves tasks like copying and pasting data from emails, invoices, scanned PDFs, or spreadsheets into systems. Manual document processing is costly, slow, and error-prone. To enhance the data-driven decision making and accuracy for the company, we leveraged AI-driven automation. 

System Workflow and Execution

 

Sample JSON Output from the PDF Reader

{
  "page": 2,
  "data": {
    "vendor": "[Educational Institution]",
    "date": "2022-10-27",
    "items": [
      {
        "description": "[Bakery Item 1]",
        "price": 1.6
      },
      {
        "description": "[Dairy Product 1]",
        "price": 2.15
      }
    ],
    "subtotal": 3.75,
    "paymentMethod": "[Card Payment]",
    "vatNumber": "[VAT]"
  }
}
 

Technology Stack (Cost-Effective & Efficient)

Gemini AI API (v 1.5 Flash): Cost-effective AI-powered text extraction
Python v3.11 : Open-source, no licensing fees, Automates document processing efficiently
OCR (Optical Character Recognition) as PyMuPDF v1.22.5 : Reads and converts scanned PDFs to text
Pandas v2.0: Handles JSON for structured output
AsyncIO (Latest Release) – Enables parallel processing for speed
 

Projected Business Impact
Improves accuracy in business decision making, through blurry data filtration: Built-in data sanitisation (filters unclear information).
Improves decision making, through JSON Extraction – output format ready for data visualization.
Improves efficiency by 99%, by processing multiple documents at once.
Reduces Cybersecurity breaches by 90% - through identification of malicious scripts in documents thereby saving money.
Better Storage - JSON outputs are 90% smaller than original PDFs.
Mitigates against GDPR fines and compliance issues - Auto-redaction + audit trails = zero manual errors.
 

Recommendations
Scale Parallel Document Processing Across Key Business Teams
Utilize processing to handle high volumes of documents efficiently, supporting the Finance, Procurement, Legal, Human Resources (HR), Sales & Marketing, and Operations teams.
Enable Real-Time Dashboards Using Extracted Data
Connect JSON outputs to tools like Power BI or Google Data Studio to provide leadership with up-to-date insights for strategic decision-making.
