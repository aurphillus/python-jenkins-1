pipeline {
    agent {
        docker {
            image 'python:3.8.12-slim-buster'
        }
    }

    stages {
        stage('Version Check') {
            steps {
                sh 'python --version'
            }
        }
        stage('Virtual Environment Setup') {
            steps {
                sh 'python -m venv venv'
                sh 'source venv/bin/activate'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r req.txt'
            }
        }
    }
}