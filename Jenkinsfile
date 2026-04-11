pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                sh 'python3 -m venv venv'
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