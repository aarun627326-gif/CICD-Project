pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                git 'https://github.com/aarun627326-gif/CICD-Project.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo Build Successful'
            }
        }
    }
}
