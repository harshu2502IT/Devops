pipeline {
    agent any

    environment {
        REPO = 'https://github.com/harshu2502IT/Devops.git'
    }

    stages {

        stage('Clone') {
            steps {
                git branch: 'main', url: "${REPO}"
            }
        }

        stage('Build') {
            steps {
                sh '''
                docker run \
                -v $PWD:/srv/jekyll \
                -v $PWD/_site:/srv/jekyll/_site \
                jekyll/builder:latest \
                /bin/bash -c "chmod -R 777 /srv/jekyll && jekyll build"
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy step here"
                // Example:
                // sh 'scp -r _site/* user@server:/var/www/html/'
            }
        }
    }
}