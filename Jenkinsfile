pipeline {
    agent any

    environment {
        IMAGE_NAME = 'my-app'
        CONTAINER_NAME = 'my-app-container'
        HOST_PORT = '8081'
        CONTAINER_PORT = '80'
    }

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
                sh 'docker build -t ${IMAGE_NAME}:v1 .'
                sh 'docker tag ${IMAGE_NAME}:v1 ${IMAGE_NAME}:latest'
            }
        }

        stage('Test') {
            steps {
                echo 'Running basic test stage...'
                sh 'test -f index.html'
                sh 'test -f Dockerfile'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying container...'
                sh '''
                docker stop ${CONTAINER_NAME} || true
                docker rm ${CONTAINER_NAME} || true
                docker run -d --name ${CONTAINER_NAME} -p ${HOST_PORT}:${CONTAINER_PORT} ${IMAGE_NAME}:latest
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully.'
        }
           failure {
            echo 'Pipeline failed. Check console output.'
         }
     }
}
