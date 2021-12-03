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

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r req.txt'
            }
        }
    }
}