pipeline {
    agent {
        docker {
            image 'python:3.11'
        }
    }

    stages {
        stage('Install') {
            steps {
                sh 'python -m venv venv'
                sh 'venv/bin/pip install -r requirements.txt'
            }
        }

        stage('Run Server Check'){
            steps {
                sh 'venv/bin/python manage.py check'
            }
        }

        stage('Done') {
            steps {
                sh 'echo Django Pipeline Success'
            }
        }
    }
}