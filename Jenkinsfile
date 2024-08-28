pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the repository
                git url: 'https://github.com/your-repo/your-project.git', branch: 'main'
            }
        }
        stage('Copy PowerShell Script') {
            steps {
                // Copy the PowerShell script to the specified location
                powershell script: '''
                    $sourcePath = "C:\\Jenkins\\workspace\\your-project\\your-script.ps1"
                    $destinationPath = "C:\\Target\\Location\\your-script.ps1"
                    Copy-Item -Path $sourcePath -Destination $destinationPath -Force
                '''
            }
        }
    }
}
