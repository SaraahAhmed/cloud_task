pipeline {
    agent any
    stages {
        stage('Clone cloud_task Repository') {
            steps {
                // Clone the cloud_task repository
                git url: 'https://github.com/SaraahAhmed/cloud_task.git', branch: 'main'
            }
        }
        stage('Clone bonusTask Repository and Run Batch File') {
            steps {
                // Clone the bonusTask repository
                dir('bonusTask') {
                    git url: 'https://github.com/SaraahAhmed/bonusTask.git', branch: 'main'
                }
                
                // Run the batch file from the cloned repository
                dir('bonusTask') {
                    bat 'CloudTask.bat'
                }
            }
        }
    }
}
