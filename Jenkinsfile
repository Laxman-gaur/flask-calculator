pipeline {
    agent any

    stages {
        stage('git clone ') {
            steps {
                sh 'https://github.com/Laxman-gaur/flask-calculator.git' 
            }
        }
        stage('change directory') {
            steps {
                sh 'cd /var/lib/jenkins/workspace/flask-calculator'
            }
        }
        stage('install the dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('deploy') {
            steps {
                sh 'pm2 start app.py' 
            }
        }
    }
}
