pipeline {
    agent any
    stages {
        stage('change directory and present working directory') {
            steps {
                sh 'git clone https://github.com/Laxman-gaur/flask-calculator.git'
                sh 'cd /var/lib/jenkins/workspace'
                sh 'cd ./ flask-calculator'
                sh 'ls'
                sh 'pwd'
            }
        }
        stage('install required dependencies') {
            steps {
                sh 'pip3 install -r requirement.txt'
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
        stage('deploy') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}
