pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling code from GitHub...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage running...'
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage running...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage placeholder...'
            }
        }
    }
}
