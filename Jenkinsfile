pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
                echo "Checked out from GitHub: ${env.GIT_URL} @ ${env.GIT_COMMIT}"
            }
        }
        stage('Verify') {
            steps {
                sh 'ls -la'
                sh 'cat README.md'
                sh 'git log --oneline -n 5'
            }
        }
    }
    post {
        success { echo 'Jenkins successfully accessed the GitHub repository.' }
    }
}
