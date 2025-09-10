pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/pourbehzad/jenkins-hello-world-app.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Installing Node.js dependencies...'
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                bat 'nohup node app.js > app.log &'
            }
        }
    }
}