pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'git@github.com:daniyaalabbas/devops-docker-linux-practice.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t abbas-nginx-app .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'docker stop abbas-container || true'
                sh 'docker rm abbas-container || true'
            }
        }

        stage('Run New Container') {
            steps {
                sh 'docker run -d -p 8080:80 --name abbas-container abbas-nginx-app'
            }
        }
    }
}

