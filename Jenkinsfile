pipeline {
    agent any
    tools{
       nodejs 'Node' 
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo Building the application...'
                sh 'npm install express'
                sh 'npm run build'
            }
            post {
                success {
                    echo 'Build successful.'
                }
                failure {
                    echo 'Build failed.'
                }
            }
        }
        stage('Test') {
            steps {
                sh 'echo Running unit tests...'
                sh 'npm test'
            }
            post {
                success {
                    echo 'Tests successful.'
                }
                failure {
                    echo 'Tests failed.'
                }
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Deploying the application...'
                sh 'npm run deploy'
            }
            post {
                success {
                    echo 'Deployment successful.'
                }
                failure {
                    echo 'Deployment failed.'
                }
            }
        }
    }
}