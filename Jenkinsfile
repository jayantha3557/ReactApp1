pipeline {
    agent any

    environment {
        NPM_CONFIG_CACHE = "${WORKSPACE}/.npm"
        PM2_EXECUTABLE = "/path/to/pm2" // Specify the full path to the pm2 executable
    }

    stages {
        stage('node info') {
            steps {
                sh "npm config ls"
            }
        }
        stage('Install node modules') {
            steps {
                sh "npm install"
            }
        }
        stage('Running tests') {
            steps {
                sh "npm test"
            }
        }
        stage('Building app') {
            steps {
                sh "npm run build"
            }
        }
        stage('Deploying app') {
            steps {
                sh "${env.PM2_EXECUTABLE} serve build 4005 --watch"
            }
        }
    }
}
