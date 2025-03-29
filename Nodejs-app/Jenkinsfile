pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'echo Building the application...'
                sh 'npm install express'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                sh 'echo Running unit tests...'
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Deploying the application...'
                sh 'npm run deploy'
            }
        }
    }
}