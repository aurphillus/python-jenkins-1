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
                #!/bin/bash
                python -m venv env
                source ./env/bin/activate
                """
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r req.txt'
            }
        }
    }
}