pipeline {
    agent any
    
    stages {
        stage('Checkout SCM') {
            steps {
                checkout scm
            }
        }
        
        stage('Install node modules') {
            steps {
                script {
                    // Replace 'nohup' with '&' to run the command in the background
                    // This is a platform-agnostic alternative
                    sh 'npm install &'
                }
            }
        }
        
        stage('Running tests') {
            steps {
                script {
                    // Replace 'nohup' with '&' to run the command in the background
                    // This is a platform-agnostic alternative
                    sh 'npm test &'
                }
            }
        }
        
        stage('Building app') {
            steps {
                script {
                    // Replace 'nohup' with '&' to run the command in the background
                    // This is a platform-agnostic alternative
                    sh 'npm run build &'
                }
            }
        }
        
        stage('Deploying app') {
            steps {
                script {
                    // Replace 'nohup' with '&' to run the command in the background
                    // This is a platform-agnostic alternative
                    sh 'pm2 start app.js &'
                }
            }
        }
    }
}

