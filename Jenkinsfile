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
                sh """
                python -m venv env
                ./env/bin/activate
                """
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'python -m pip install -r req.txt'
            }
        }
    }
}