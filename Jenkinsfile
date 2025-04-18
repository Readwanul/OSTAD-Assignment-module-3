pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning the repository...'
                checkout scm
            }
        }

        stage('Install') {
            steps {
                echo ' Installing dependencies...'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo ' Running tests...'
                sh 'npm run check'
            }
        }
    }

    post {
        always {
            echo '✅ Build finished.'
        }
    }
}
