pipeline {
    agent any
    stages {
        stage('git clone, change directory and present working directory') {
            steps {
                sh 'cd /var/lib/jenkins/workspace'
                sh 'git clone https://github.com/Laxman-gaur/flask-calculator.git'
                sh 'cd ./flask-calculator'
                sh 'ls'
                sh 'pwd'
            }
        }
        stage('install required dependencies') {
            steps {
                sh 'pip3 install -r requirements.txt'
            }
        }
        stage('deploy') {
            steps {
                sh 'pm2 start app.py --interpreter python3'
            }
        }
    }
}
