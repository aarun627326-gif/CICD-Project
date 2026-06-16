stage('SonarQube Analysis') {
    steps {
        script {
            def scannerHome = tool 'sonar-scanner'

            withSonarQubeEnv('SonarQube') {
                bat """
                "${scannerHome}\\bin\\sonar-scanner.bat" -Dsonar.projectKey=CICD-Project -Dsonar.projectName=CICD-Project -Dsonar.sources=. -Dsonar.sourceEncoding=UTF-8
                """
            }
        }
    }
}































































