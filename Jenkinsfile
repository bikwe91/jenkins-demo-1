pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling code from GitHub...'
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t my-app .'
            }
        }

        stage('Run Container') {
            steps {
                echo 'Running container...'
                sh 'docker rm -f my-app-container || true'
                sh 'docker run -d --name my-app-container -p 8081:80 my-app'
            }
        }
    }
}
