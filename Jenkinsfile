pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Code checked out from GitHub'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'python3 --version'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'echo Building Docker Image'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo Deploying Application'
            }
        }
    }
}