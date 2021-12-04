pipeline {
    agent any

    stages {
        stage('Setting up of Virtual Environment') {
            steps {
                sh 'python3 -m venv venv'
                sh 'source venv/bin/activate'
            }
        }
        stage('Installing Python Dependencies') {
            steps {
                sh 'pip install -r req.txt'
            }
        }

        stage('Check if the user is root') {
            steps {
                sh 'id -u'
            }
        }

        stage('Currenr Working Directory') {
            steps {
                sh 'pwd'
            }
        }

        stage('Find which shell is used') {
            steps {
                sh 'echo $SHELL'
            }
        }
    }
}