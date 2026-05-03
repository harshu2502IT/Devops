pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/harshu2502IT/Devops.git'
            }
        }

        stage('Clone') {
            steps {
                bat 'echo Cloning repository...'
            }
        }

        stage('Build') {
            steps {
                bat 'echo Building project...'
            }
        }

        stage('Test') {
            steps {
                bat 'echo Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                echo Deploying project to XAMPP...
                if not exist C:\\xampp\\htdocs mkdir C:\\xampp\\htdocs
                xcopy * C:\\xampp\\htdocs\\ /E /H /C /I /Y
                '''
            }
        }
    }
}