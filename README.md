Google Form Auto Notifier

An automated email notification system built with n8n that instantly sends alerts when new responses are submitted through Google Forms. This workflow monitors Google Sheets for new entries and triggers personalized email notifications automatically.

🚀 Features
•	Real-time Monitoring: Checks Google Sheets every minute for new form responses
•	Instant Notifications: Sends email alerts immediately when new data is detected
•	Cloud-based: Runs 24/7 on n8n Cloud without requiring local setup
•	Easy Configuration: Simple setup with Google Sheets and email integration
•	Customizable Messages: Personalized email content for each notification

🏗️ Workflow Architecture
Google Sheets Trigger         →          Email Notification Node
           ↓                                     ↓
- Monitors sheet every min              - Sends custom email
- Detects new rows                      - Uses JSON property for recipient
- Triggers on row addition              - Text-based email format

📋 Prerequisites
•	n8n Cloud account (free tier available)
•	Google account with access to Google Sheets
•	Google Form connected to Google Sheets
•	Email service for sending notifications

⚙️ Configuration Details
Google Sheets Trigger Node
•	Resource: Google Sheets
•	Operation: Trigger on Row Added
•	Spreadsheet: Your Google Form responses spreadsheet
•	Sheet: "Form responses 1" (Sheet #1)
•	Polling Interval: Every 1 minute
•	Watch Mode: Active monitoring
Email/Message Node
•	Resource: Send Message
•	Operation: Send
•	Recipient: JSON property linked to email field
•	Email Type: Text format
•	Message: Custom notification content

🛠️ Setup Instructions
1. Import Workflow
1.	Download the “GoogleForm-AutoNotifier.json” file from the /workflow directory
2.	In your n8n Cloud dashboard, click "Import from File"
3.	Select the downloaded JSON file
4.	The workflow will be imported with all node configurations
2. Configure Google Sheets Connection
1.	Click on the Google Sheets Trigger node
2.	Authenticate with your Google account
3.	Select your Google Form response spreadsheet
4.	Choose "Form responses 1" as the sheet
5.	Set polling to "Every Minute"
3. Configure Email Node
1.	Click on the Email/Message node
2.	Set up your email service credentials
3.	Configure the recipient email using JSON property
4.	Customize your notification message
5.	Test the connection
4. Activate Workflow
1.	Click the "Active" toggle in the top-right corner
2.	The workflow will now run continuously
3.	Monitor the execution log for successful triggers

📧 Email Notification Sample
When a new form response is submitted, recipients receive an email like:
Subject: New Google Form Response Received
“
Hello,

A new response has been submitted to your Google Form.

Response details have been recorded in your Google Sheets.

Please check your spreadsheet for the complete submission.

Best regards,
Auto Notifier System
“

🔄 How It Works
1.	Form Submission: User submits Google Form
2.	Sheet Update: Response automatically added to Google Sheets
3.	Trigger Detection: n8n monitors sheet every minute for new rows
4.	Email Dispatch: When new row detected, email notification sent instantly
5.	Continuous Monitoring: Process repeats automatically 24/7

💡 Use Cases
•	Lead Generation: Instant notification for new business inquiries
•	Event Registration: Real-time alerts for event sign-ups
•	Customer Feedback: Immediate notification of survey responses
•	Contact Forms: Instant alerts for website contact submissions
•	Survey Collection: Real-time monitoring of research responses

🔧 Customization Options
•	Message Content: Modify email templates in the message node
•	Polling Frequency: Adjust trigger interval (1 min to hours)
•	Multiple Recipients: Add multiple email addresses
•	Conditional Logic: Add filters for specific form responses
•	Rich Formatting: Switch to HTML email format for styling

📊 Benefits
•	No Code Required: Visual workflow builder, no programming needed
•	24/7 Automation: Runs continuously in the cloud
•	Cost Effective: Uses free n8n Cloud tier
•	Scalable: Handles unlimited form responses
•	Reliable: Enterprise-grade cloud infrastructure

🚨 Important Notes
•	Ensure your n8n workflow is set to "Active" mode
•	The workflow runs continuously even when browser is closed
•	Monitor your email sending limits based on your email service
•	Keep Google Sheets permissions properly configured

📝 License
This project is open source and available under the MIT License.

🔗 Related Resources
•	n8n Documentation
•	Google Sheets API
•	n8n Community

📞 Support
If you encounter any issues or have questions:
•	Check the n8n community forums
•	Review Google Sheets API documentation
•	Open an issue in this repository
________________________________________
⭐ Star this repository if you find it helpful! ⭐

