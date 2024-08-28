pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the repository
                git url: 'https://github.com/Ajaypatil266/TestRepo.git', branch: 'main'
            }
        }
        stage('Copy PowerShell Script') {
            steps {
                // Copy the PowerShell script to the specified location
                powershell script: '''
                    $sourcePath = "D:\\Study\\Jenkin\\HelloWord.ps1"
                    $destinationPath = "D:\\Temp\\HelloWord.ps1"
                    Copy-Item -Path $sourcePath -Destination $destinationPath -Force
                '''
            }
        }
    }
}
