pipeline {
    agent any

    stages {

        stage('Verify Environment') {
            steps {
                sh 'pwd'
                sh 'ls -la'
                sh 'docker --version'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t flask-app:latest .'
            }
        }

        stage('Verify Image') {
            steps {
                sh 'docker images | grep flask-app'
            }
        }

    }

    post {
        success {
            echo 'Docker image built successfully!'
        }

        failure {
            echo 'Build failed. Check console output.'
        }
    }
}
