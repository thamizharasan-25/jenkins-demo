pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/thamizharasan-25/jenkins-demo.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo Building...'
            }
        }
        stage('Test') {
            steps {
                sh 'echo Testing...'
            }
        }
    }
}
