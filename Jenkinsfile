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
                bat 'python -m pip install -r app\\requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'pytest app\\test_app.py'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t flask-cicd:%BUILD_NUMBER% .'
            }
        }

        stage('Deploy with Docker Compose') {
            steps {
                bat 'docker compose up -d'
            }
        }
    }
}