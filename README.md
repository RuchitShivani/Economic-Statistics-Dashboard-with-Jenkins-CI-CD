# 🌍 Economic Stastics Dashboard with Jenkins CI/CD

This project is a simple and colorful web-based dashboard that displays GDP statistics for major countries using interactive charts — built with HTML, CSS, JavaScript, and Chart.js, and deployed locally using Jenkins.

## 📊 Features

- Interactive bar chart of 2023 GDP data
- Clean and modern UI
- Simple frontend-only project
- Automated deployment using Jenkins
- No GitHub or backend required

## 🚀 Tech Stack

- HTML5 + CSS3
- JavaScript (Vanilla)
- [Chart.js](https://www.chartjs.org/) for interactive visualization
- Jenkins for CI/CD


🧱 Step-by-Step Setup Instructions
✅ 1. Create Project Folder and HTML File
Open PowerShell and run:

powershell
Copy
Edit
mkdir C:\Users\Ruchit\frontend-project
notepad C:\Users\Ruchit\frontend-project\index.html
Paste the HTML code (from previous response) into the Notepad window and save.

✅ 2. Create Deployment Folder
This is where Jenkins will copy the file:

powershell
Copy
Edit
mkdir C:\Users\Ruchit\deployment-folder
✅ 3. Test the HTML
To preview it without Jenkins:

powershell
Copy
Edit
start C:\Users\Ruchit\frontend-project\index.html
✅ 4. Open Jenkins and Create a Pipeline Job
Go to Jenkins: http://localhost:8080

Click "New Item".

Name it: GDP-Dashboard-Pipeline.

Select Pipeline and click OK.

✅ 5. Add Pipeline Script
In the job config page:

Scroll to Pipeline section.

Choose Pipeline script.

Paste the following code:

groovy
Copy
Edit
pipeline {
  agent any
  stages {
    stage('Deploy') {
      steps {
        bat 'xcopy /Y /I C:\\Users\\Ruchit\\frontend-project\\index.html C:\\Users\\Ruchit\\deployment-folder\\'
      }
    }
  }
}
Click Save.

✅ 6. Run the Jenkins Job
Click Build Now on the left.

If successful, Jenkins will copy your dashboard file to the deployment-folder.

✅ 7. View the Dashboard
Open the file in your browser:

powershell
Copy
Edit
start C:\Users\Ruchit\deployment-folder\index.html


   
![Screenshot 2025-05-06 171618](https://github.com/user-attachments/assets/58ae93cd-f2c9-48de-87cd-90662d2cedb0)
![Screenshot 2025-05-06 171655](https://github.com/user-attachments/assets/be3d2a8c-3d2d-4803-ab36-47ae1cebf19c)
