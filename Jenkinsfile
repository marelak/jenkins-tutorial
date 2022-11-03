pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                retry(5) {
                    bat 'flakey-deploy.bat'
                }

                timeout(time: 1, unit: 'MINUTES') {
                    bat 'health-check.bat'
                }
            }
        }
    }
}
