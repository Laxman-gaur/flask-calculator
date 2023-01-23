pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/Laxman-gaur/flask-calculator.git', branch: 'main'
            }
        }
        stage('change directory and present working directory') {
            steps {
                sh 'cd /home/ubuntu/flask-calculator'
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
                sh 'pm2 start app.py'
            }
        }
    }
}
