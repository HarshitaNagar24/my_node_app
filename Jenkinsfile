node {
    // Variables
    def appName = "my_node_app"
    
    stage('Checkout') {
        echo 'Checking out the code...'
        checkout scm
    }
    
    stage('Install Dependencies') {
        echo 'Installing Node.js dependencies...'
        sh 'npm install'
    }

    stage('Run Tests') {
        echo 'Running tests...'
        sh 'npm test'
    }

    stage('Build') {
        echo 'Building the application...'
        sh 'npm run build'
    }

    stage('Deploy') {
        echo 'Simulating deployment...'
        sh 'echo "Deploying application to server (e.g., Docker, AWS, etc.)"'
    }
}
