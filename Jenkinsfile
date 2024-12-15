pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the code...'
                checkout scm
            }
        }
        
        stage('Install Dependencies') {
            steps {
                echo 'Installing Node.js dependencies...'
                sh 'npm install'
            }
        }

        stage('Fix Permissions for Jest') {
            steps {
                echo 'Fixing permissions for Jest...'
                sh 'chmod +x node_modules/.bin/jest' // Fix permissions for jest binary
            }
        }
        
        stage('Run Tests') {
            steps {
                echo 'Running tests...'
                sh 'npx jest' // Run tests with npx
            }
        }
    }
}
