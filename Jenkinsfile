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

                    withSonarQubeEnv('SonarQube') {
                        bat """
                        "${scannerHome}\\bin\\sonar-scanner.bat" ^
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
}
















































































