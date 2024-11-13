# Email-Attachment-Analysis-Script

This project is a Python-based solution for scanning email attachments to detect potential malware and other security threats. Using IMAP to access emails, the script downloads attachments, scans for malware indicators, and generates a comprehensive report in CSV format.

**Project Overview**
Email attachments are a major source of cyber threats, including phishing, malware, and ransomware. This project automates the process of analyzing email attachments without relying on third-party APIs or antivirus software. It checks attachments for password protection, scans for malicious content, and detects obfuscated data, providing a self-contained and privacy-conscious approach.

**Features**
* IMAP-based Email Connection: Fetches emails and attachments directly from the inbox.
* Malware Detection: Identifies malicious files by comparing attachment hashes against a known
  malware list.
* Password Protection Check: Flags PDF files that are password-protected.
* Suspicious Content Detection: Flags risky file types (e.g., .exe, .js) and obfuscated PDF content.
* CSV Report: Generates a detailed report with information on each email and attachment.

**Setup and Installation**
**Prerequisites:**
Make sure you have the following installed:
* Python 3.7+
* pip for managing Python packages

**Required Libraries:**
Install the required libraries by running: "pip install -r requirements.txt"

**The 'requirements.txt' file should include:**
* imaplib
* email
* pandas
* hashlib
* PyPDF2
* io
* time

**Email Account Setup:**
1. Set up an email account that supports IMAP (e.g., Gmail).
2. If your email provider requires app-specific passwords for IMAP, set one up and use it in the
   script.

**Running the Project**
* Step 1: Clone the Repository
  'git clone https://github.com/om-rk23/email-attachment-analysis.git'
  'cd email-attachment-analysis'

* Step 2: Configure Email Credentials
  In the script, set your email address and app-specific password in the placeholders:
   email_user = "youremail@example.com"
  email_pass = "yourpassword"

* Step 3: Execute the Script
  Run the script to start fetching and scanning email attachments:
  'python email_attachment_analysis.py'

  The script will connect to your email account, retrieve emails, and begin analyzing attachments.
  Results will be saved in a CSV report.

* Step 4: Review the Report
  A CSV file (attachment_report.csv) will be generated, summarizing each attachment's properties
  and whether it was flagged as malicious or password-protected.

**Project Structure**
├── email_attachment_analysis.py     # Main script for email processing and attachment analysis
├── requirements.txt                 # List of required libraries
└── attachment_report.csv            # Output report with analysis results (generated after script runs)

**Example Output**
* The CSV report includes:
* Sender Information: Email address of the sender
* File Type: MIME type of the attachment
* Password Protection: Whether a PDF file is password-protected
* Malware Detection: Indicates if the attachment is potentially malicious based on hash and file
  type

**This README.md provides installation instructions, usage steps, and an overview of the project features.**
