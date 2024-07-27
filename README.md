### Merit Orchestrator
MeritOrchestrator is a streamlined system designed to automate the generation and distribution of certificates for merit students and event participants. This tool efficiently processes data from Excel spreadsheets, creates personalized certificates, and sends them directly to the recipients' email addresses.

```markdown

**How It Works:**
Data Upload: Upload your Excel sheet containing student names and email addresses.
Template Selection: Choose or customize a certificate template to fit your needs.
Certificate Generation: The system generates certificates for each recipient based on the data provided.
Email Distribution: Automatically sends the certificates to the specified email addresses.

**Technologies Used:**
Python: For scripting the automation and data processing.
Pandas: To handle and process Excel data.
SMTP: For sending emails.

# Certificate Generation and Upload to Google Drive

This repository contains the code to generate certificates from a CSV file using a DOCX template and upload them to Google Drive.

## Library Installation

1. Install LibreOffice Writer:
   ```bash
   !apt-get install -y libreoffice-writer
   ```

2. Install necessary Python packages:
   ```bash
   !pip install gspread oauth2client pandas python-docx google-auth google-auth-oauthlib google-auth-httplib2
   ```

## File Upload

1. Use the following code to upload your service account JSON file, CSV file, and DOCX template file:
   ```python
   from google.colab import files
   uploaded = files.upload()
   ```

2. The paths of these files will be dynamically set based on the uploaded files.

## Path Adjustments

Make sure to update the paths to the service account JSON file, CSV file, and DOCX template in your code to match the files uploaded to Colab.

## Folder ID

Replace `'16ah9GxctJ84RQCqyH4_i2uXjwbESgH73'` with your actual Google Drive folder ID where you want to upload the certificates.

## Running in Google Colab

This code is ready to be run in Google Colab and should work seamlessly with your existing setup.

## Obtaining the `service_account.json` File

To get the `service_account.json` file for Google Cloud services, you'll need to create a service account in the Google Cloud Console and generate a key for it. Follow these steps:

1. **Go to the Google Cloud Console:**  
   Open your web browser and go to the [Google Cloud Console](https://console.cloud.google.com/).

2. **Select or Create a Project:**  
   Select an existing project or create a new one.

3. **Navigate to the IAM & Admin section:**  
   In the left-hand navigation menu, go to **IAM & Admin > Service Accounts**.

4. **Create a Service Account:**  
   Click on the `+ CREATE SERVICE ACCOUNT` button at the top of the page.  
   Enter a name and description for your service account.  
   Click **Create**.

5. **Assign Roles to the Service Account:**  
   In the Service account permissions step, assign the necessary roles to the service account. For example, if you are working with Google Drive, you might need the Drive API roles.  
   Click **Continue**.

6. **Create a Key for the Service Account:**  
   In the Grant users access to this service account step, you can skip it and click **Done**.  
   After creating the service account, you'll see it listed. Click on the service account name to open its details.  
   Go to the **Keys** tab.  
   Click on **Add Key > Create New Key**.  
   Choose the JSON key type.  
   Click **Create**. The JSON key file will be downloaded to your computer.

7. **Store the `service_account.json` file securely:**  
   Save the downloaded `service_account.json` file in a secure location. You will use this file to authenticate your applications with Google Cloud services.

Now, you have the `service_account.json` file needed for accessing Google Cloud services programmatically.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/MeritOrchestrator.git
   ```

2. Navigate to the project directory:
   ```bash
   cd MeritOrchestrator
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

Follow the instructions in the Usage Guide to set up and run the application.
```

This Markdown code provides clear and well-organized instructions, with formatting for code blocks, links, lists, and inline code. Remember to replace `"your-username"` in the clone URL with your actual GitHub username.
