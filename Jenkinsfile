pipeline {
    agent any

    tools {
        sonarQubeScanner 'sonar-scanner'
    }

    stages {

        stage('Git Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/aarun627326-gif/CICD-Project.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build Successful'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    bat """
                    sonar-scanner ^
                    -Dsonar.projectKey=CICD-Project ^
                    -Dsonar.projectName=CICD-Project ^
                    -Dsonar.sources=. ^
                    -Dsonar.sourceEncoding=UTF-8
                    """
                }
            }
        }
    }
}
















































































