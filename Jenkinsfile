pipeline {
    agent any

    stages {
        stage('Install node modules') {
            steps {
                bat 'npm install'
                // Add more bat commands as needed
            }
        }
        stage('Running tests'){
            steps {
                bat "npm test"
            }
        }
        stage('Building app'){
            steps{
                bat "npm run build"
            }
        }
        stage('Deploying app') {
            steps {
                bat "pm2 serve build 4005 --watch"
            }
        }
    }
}
