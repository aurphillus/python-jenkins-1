pipeline {
    agent any

    stages {
        stage('Version Check') {
            steps {
                sh 'python --version'
            }
        }
        stage('Check which user is running'){
            steps {
                sh 'whoami'
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