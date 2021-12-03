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
        stage('Python Configuration') {
            steps {
                sh """#!/bin/bash

                python -m venv env
                source ./env/bin/activate
                pip install -r req.txt
                python main.py
                """
            }
        }
    }
}