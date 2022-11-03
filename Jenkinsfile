pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                retry(5) {
                    bat 'echo Hi'
                }

                timeout(time: 1, unit: 'MINUTES') {
                    bat 'echo Right back at ya'
                }
            }
        }
    }
}
