# Colab_usage
1.colab&amp;google_dirve
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

#2.how to import to colab:
#(1). FOR WHOLE PROJECT:
from google.colab import drive
drive.mount('/content/drive')#then link to your google drive
#(2)进入到自己创建的文件夹或者重新创建一个文件夹（用来存储即将要导入的GitHub项目，不然默认导入的位置是云盘的根目录下，不方便管理）
#(3)添加一个代码输入框，输入命令：!git clone 项目的Git链接
#!git clone #your project https
!git clone https://github.com/TammyLing/Typhoon-forecasting.git
!rm -rf sigver #if u want to delete some folder(replace'sigver')
#从临时环境中copy到Google drive:
%cd /content/drive/MyDrive/
!git clone https://github.com/TammyLing/Typhoon-forecasting.git
