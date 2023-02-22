pipeline {
    agent any
    stages {
        stage('change directory and present working directory') {
            steps {
                sh 'cd /var/lib/jenkins/workspace/flask-calculator'
                sh 'pwd'
            }
        }
        stage('install required dependencies') {
            steps {
                sh 'pip3 install -r requirements.txt'
            }
        }
        stage ('approval') {
            input {
                message "do you want to proceed for production deployment ?"
            }
            steps {
                sh "deploy to production"
            }
        }
        stage('Deploy') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}
