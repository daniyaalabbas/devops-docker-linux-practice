pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t nginx-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker stop nginx-container || true
                docker rm nginx-container || true
                docker run -d -p 8085:80 --name nginx-container nginx-app
                '''
            }
        }
    }
}

