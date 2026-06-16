pipeline {
    agent any

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
                script {
                    def scannerHome = tool 'sonar-scanner'

                    echo "Scanner Home: ${scannerHome}"

                    bat "dir \"${scannerHome}\\bin\""

                    withSonarQubeEnv('SonarQube') {
                        bat "\"${scannerHome}\\bin\\sonar-scanner.bat\" --version"
                    }
                }
            }
        }
    }
}















































