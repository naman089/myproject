pipeline {
    agent any
    stages {
        stage('Install') {
            steps {
                bat 'python -m venv venv'
                bat 'venv\\Scripts\\activate && pip install -r requiremets.txt'

            }
        }
        stage('Run Server Check'){
            steps {
                bat 'venv\\Scripts\\activate && python manage.py check'
            }
        }
        stage('Done') {
            steps {
                bat 'echo Djano Pipline Success'
            }
        }
    }
}