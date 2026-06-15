pipeline {
    agent any

    stages {

        stage('Git Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/aarun627326-gif/CICD-Project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t arun-nginx-app .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 8081:80 --name arun-nginx arun-nginx-app'
            }
        }
    }
}






































