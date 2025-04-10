# GLdailyReconciliationProcess

AI Report Builder
Overview
The AI Report Builder is a web-based application that allows users to upload CSV files to generate automated reports using the Integrail AI platform. The application connects to an Integrail agent that processes financial data and generates comprehensive cash management reports for banking operations.
Features

Simple file upload interface for CSV data
Real-time processing status updates
Formatted display of generated reports
Download capability for reports
Integration with Integrail AI agent for data processing
Clean, responsive design that works across devices

Technical Architecture
The application consists of two main components:

Front-End Landing Page: A responsive HTML, CSS, and JavaScript application that handles file uploads and displays results
Back-End Processing: An Integrail AI agent that processes CSV files and generates analysis reports

Front-End Components

File Upload Handler: Manages CSV file selection and submission
API Integration: Connects to the Integrail API for processing
Status Tracker: Monitors processing progress with real-time updates
Report Display: Formats and presents generated reports
Download Module: Allows users to save reports locally

Back-End Components (Integrail Agent)

CSV Parser: Reads and processes CSV file data
Analysis Engine: Analyzes financial data for anomalies
Report Generator: Creates structured reports based on analysis
Email Notifier: Sends report results via email

Installation

Clone the repository:

git clone https://github.com/your-org/report-builder.git

Open the index.html file in your web browser or host it on a web server.
No additional dependencies are required for the front-end.

Configuration
The application requires configuration of the following parameters in the index.html file:
javascript// API endpoints
const executeEndpoint = 'https://cloud.integrail.ai/api/YOUR_ACCOUNT_ID/agent/YOUR_AGENT_ID/execute';
const statusEndpointTemplate = 'https://cloud.integrail.ai/api/YOUR_ACCOUNT_ID/agent/{{executionId}}/status';

// Bearer token for authorization
const bearerToken = 'YOUR_BEARER_TOKEN';
Replace the placeholders with your actual Integrail account information.
Usage

Open the application in a web browser
Click on the upload area or the "Choose File" button to select a CSV file
Once a file is selected, click "Generate Report"
Wait for the processing to complete (progress will be displayed)
View the generated report on the page
Click "Download Report" to save the report as a text file

CSV File Format
The application expects CSV files with the following format:

Banking general ledger data
Daily account balances for branches
Currency information
Cash vault balances

Example structure:
BranchID,Date,AccountType,Currency,Balance,Limit
102,2025-04-10,Cash Vault,KWD,15000,30000
205,2025-04-10,Cash Vault,KWD,55000,30000
...
API Integration
The application interacts with the Integrail API using the following endpoints:

Execute Endpoint:

POST https://cloud.integrail.ai/api/YOUR_ACCOUNT_ID/agent/YOUR_AGENT_ID/execute
Used to submit the CSV file for processing


Status Endpoint:

GET https://cloud.integrail.ai/api/YOUR_ACCOUNT_ID/agent/{{executionId}}/status
Used to check the status of a processing job



Authentication is performed using a bearer token in the request headers.
Troubleshooting
Common issues and solutions:

File Upload Errors: Ensure the file is a valid CSV format
Processing Errors: Check that the CSV structure matches the expected format
Authorization Errors: Verify that the bearer token is valid and has not expired
API Connection Errors: Confirm that the API endpoints are correctly configured


Contact
For questions or support, please contact me.
