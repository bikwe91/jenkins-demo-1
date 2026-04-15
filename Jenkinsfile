pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/bikwe91/jenkins-demo-1.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f my-app-container || true'
                sh 'docker run -d --name my-app-container -p 8081:80 my-app'
            }
        }
    }
}
