# Colab_usage
colab&amp;google_dirve
This tutorial demonstrates how to upload files to Google Drive using a service account, including support for resumable uploads in case of network interruptions.

Key Points:
Service Account Setup: Create a service account and download the JSON credentials file.
Resumable Uploads: The code allows you to continue uploads after a network disconnection.
This makes it useful for automated file management and ensuring reliable uploads.

API setting：
Steps to Download and Use the Private Key
Download the Private Key File
Open the link: Google Cloud Console, and find your project.
Navigate to “APIs & Services” > “Credentials” to create a service account and download the credentials file in JSON format.
Save the Credentials File
Save the downloaded JSON file in your Python project directory. Copy the file path, as you will need to paste it in your code later.
Update the Code with the File Name
In your code, replace your_credentials.json with the name of the JSON file you downloaded. For example, if the file name is my_credentials.json, you should update it to:
CREDENTIALS_FILE = 'my_credentials.json'

the whole code is in "continue_download"
