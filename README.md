<!DOCTYPE html>
<html>
<head>
    <title>Certificate Generation and Upload to Google Drive</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
        }
        h1 {
            color: #333;
        }
        h2 {
            color: #555;
        }
        code {
            background-color: #f4f4f4;
            padding: 2px 4px;
            border-radius: 4px;
            font-family: monospace;
        }
        pre {
            background-color: #f4f4f4;
            padding: 10px;
            border-radius: 4px;
            overflow-x: auto;
        }
        ul {
            list-style-type: disc;
            margin: 0;
            padding-left: 20px;
        }
        .bash {
            background-color: #f4f4f4;
            padding: 10px;
            border-radius: 4px;
            font-family: monospace;
        }
    </style>
</head>
<body>

    <h1>Certificate Generation and Upload to Google Drive</h1>
    <p>This repository contains the code to generate certificates from a CSV file using a DOCX template and upload them to Google Drive.</p>

    <h2>Library Installation</h2>
    <p>1. Install LibreOffice Writer:</p>
    <pre><code>!apt-get install -y libreoffice-writer</code></pre>

    <p>2. Install necessary Python packages:</p>
    <pre><code>!pip install gspread oauth2client pandas python-docx google-auth google-auth-oauthlib google-auth-httplib2</code></pre>

    <h2>File Upload</h2>
    <p>1. Use the following code to upload your service account JSON file, CSV file, and DOCX template file:</p>
    <pre><code>from google.colab import files
uploaded = files.upload()</code></pre>

    <p>2. The paths of these files will be dynamically set based on the uploaded files.</p>

    <h2>Path Adjustments</h2>
    <p>Make sure to update the paths to the service account JSON file, CSV file, and DOCX template in your code to match the files uploaded to Colab.</p>

    <h2>Folder ID</h2>
    <p>Replace <code>'16ah9GxctJ84RQCqyH4_i2uXjwbESgH73'</code> with your actual Google Drive folder ID where you want to upload the certificates.</p>

    <h2>Running in Google Colab</h2>
    <p>This code is ready to be run in Google Colab and should work seamlessly with your existing setup.</p>

    <h2>Obtaining the service_account.json File</h2>
    <p>To get the <code>service_account.json</code> file for Google Cloud services, you'll need to create a service account in the Google Cloud Console and generate a key for it. Follow these steps:</p>

    <ul>
        <li><strong>Go to the Google Cloud Console:</strong><br>
        Open your web browser and go to the <a href="https://console.cloud.google.com/">Google Cloud Console</a>.</li>
        
        <li><strong>Select or Create a Project:</strong><br>
        Select an existing project or create a new one.</li>
        
        <li><strong>Navigate to the IAM & Admin section:</strong><br>
        In the left-hand navigation menu, go to <strong>IAM & Admin > Service Accounts</strong>.</li>
        
        <li><strong>Create a Service Account:</strong><br>
        Click on the <code>+ CREATE SERVICE ACCOUNT</code> button at the top of the page.<br>
        Enter a name and description for your service account.<br>
        Click <strong>Create</strong>.</li>
        
        <li><strong>Assign Roles to the Service Account:</strong><br>
        In the Service account permissions step, assign the necessary roles to the service account. For example, if you are working with Google Drive, you might need the Drive API roles.<br>
        Click <strong>Continue</strong>.</li>
        
        <li><strong>Create a Key for the Service Account:</strong><br>
        In the Grant users access to this service account step, you can skip it and click <strong>Done</strong>.<br>
        After creating the service account, you'll see it listed. Click on the service account name to open its details.<br>
        Go to the <strong>Keys</strong> tab.<br>
        Click on <strong>Add Key > Create New Key</strong>.<br>
        Choose the JSON key type.<br>
        Click <strong>Create</strong>. The JSON key file will be downloaded to your computer.</li>
        
        <li><strong>Store the service_account.json file securely:</strong><br>
        Save the downloaded <code>service_account.json</code> file in a secure location. You will use this file to authenticate your applications with Google Cloud services.</li>
    </ul>

    <p>Now, you have the <code>service_account.json</code> file needed for accessing Google Cloud services programmatically.</p>

    <h2>Installation</h2>
    <p>1. Clone the repository:</p>
    <pre class="bash"><code>git clone https://github.com/teja-palleti/Merit-Orchestrator.git</code></pre>

    <p>2. Navigate to the project directory:</p>
    <pre class="bash"><code>cd MeritOrchestrator</code></pre>

    <p>3. Install dependencies:</p>

</body>
</html>
