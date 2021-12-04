pipeline {
    agent any

    stages {
        stage('Python Invocation Stage') {
            steps {
                sh """#!/bin/bash
                python3 -n venv venv
                source venv/bin/activate
                pip install -r requirements.txt
                python main.py
                """
            }
        }

        stage('Output Upload Stage') {
            steps {
                sh """#!/bin/bash
                echo "Uploading output to S3"
                """
            }
        }
    }
}