pipeline {
    agent any
    tools {
        nodejs 'Nodejs20'
    }

    stages {
        stage('Node Version check') {
            steps {
                // Install Node.js and npm
                // This assumes you have Node.js and npm installed on your Jenkins agent
                sh 'node -v'
            }
        }

        stage('NPM Version') {
            steps {
                // NPM Version
                sh 'npm -v'
            }
        }
        
        stage('Build Job') {
            steps {
                // Build the Angular application
                sh 'npm i'
            }
        }
    }
    post {
        success {
            // You can add post-build actions here
            echo 'Build and deployment successful!'
        }

        failure {
            // You can add actions to be executed if the build fails
            echo 'Build or deployment failed!'
        }
    }
}
