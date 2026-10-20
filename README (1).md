# **AI Invoice & Document Processing Automation**

An AI-powered invoice processing workflow built with **n8n, Google Gemini, Google Drive, and Google Sheets**. This project automates invoice data extraction, basic validation through workflow logic, duplicate detection, and spreadsheet record management.

## **Overview**

Manually processing invoices can be repetitive and time-consuming. This workflow uses AI to extract important invoice information from PDF documents and automatically organize the results in Google Sheets.

## **Features**

* **Automated invoice intake:** Monitors a designated Google Drive folder for incoming invoices.  
* **PDF text extraction:** Extracts readable text from invoice PDF files.  
* **AI-powered data extraction:** Uses Google Gemini to identify key invoice information.  
* **Structured output:** Organizes extracted data into individual fields.  
* **Duplicate detection:** Checks invoice records against Google Sheets to help prevent duplicate entries.  
* **Automated record management:** Adds processed invoice details to Google Sheets.  
* **Error recovery:** Configures retries for temporary AI service failures.

## **Technologies Used**

* **n8n** — Workflow automation  
* **Google Gemini** — AI-powered invoice data extraction  
* **Google Drive** — Invoice file storage and intake  
* **Google Sheets** — Invoice database and record management  
* **JavaScript** — Parsing AI-generated JSON output

## **Workflow**

1. A new invoice PDF is detected in Google Drive.  
2. The PDF is downloaded.  
3. Invoice text is extracted from the document.  
4. Google Gemini identifies the required invoice fields.  
5. A JavaScript Code node parses the AI-generated JSON.  
6. The workflow checks for an existing invoice number.  
7. New invoice records are sent to Google Sheets.

## **Invoice Fields Extracted**

* Invoice number  
* Supplier name  
* Invoice date  
* Due date  
* Currency  
* Subtotal  
* Tax  
* Total amount  
* Payment status

## **Example**

| Field | Example Value |
| ----- | ----- |
| Invoice Number | INV-1003 |
| Supplier | BlueWave Technology Supplies |
| Currency | USD |
| Subtotal | 250.00 |
| Tax | 20.00 |
| Total Amount | 270.00 |
| Payment Status | Unpaid |

*Example data is provided for demonstration purposes.*

## **Setup**

1. Create an n8n workflow.  
2. Connect Google Drive and configure the folder trigger.  
3. Configure the Google Drive download and PDF extraction nodes.  
4. Connect Google Gemini and configure the invoice extraction prompt.  
5. Add a JavaScript Code node to parse the structured output.  
6. Connect Google Sheets and configure the invoice database.  
7. Configure duplicate detection using the invoice number.  
8. Test the workflow using sample invoice PDFs.

## **Important Notes**

* Configure credentials securely using n8n's credential manager.  
* Never upload API keys, access tokens, or private invoice documents to GitHub.  
* AI-generated data should be reviewed before being used for financial decisions.  
* Duplicate detection depends on the workflow's matching logic and should be tested with repeated invoice numbers.

## **What I Learned**

* Building multi-step AI automation workflows in n8n  
* Connecting AI models with Google Workspace services  
* Extracting structured data from PDF documents  
* Parsing JSON using JavaScript  
* Implementing duplicate detection logic  
* Handling temporary API failures with retry settings

## **Future Improvements**

* Add invoice amount and required-field validation.  
* Create automated alerts for failed processing.  
* Generate payment reminders for overdue invoices.  
* Add a human approval step before saving sensitive financial records.  
* Export and document the n8n workflow for easier setup.

## **Author**

**Umair Ali**  
Frontend Developer | AI Automation Learner

GitHub: [https\://github.com/umairdevh7](https://github.com/umairdevh7)

---

Built as a hands-on project to explore practical AI-powered business process automation.

