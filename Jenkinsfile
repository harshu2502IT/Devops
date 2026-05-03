pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/harshu2502IT/Devops.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build successful'
                bat 'dir'
            }
        }

        stage('Deploy to XAMPP') {
            steps {
                bat '''
                rmdir /S /Q C:\\xampp\\htdocs\\DevOps_project
                mkdir C:\\xampp\\htdocs\\DevOps_project
                xcopy /E /I /Y * C:\\xampp\\htdocs\\DevOps_project
                '''
            }
        }
    }
}