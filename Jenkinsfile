pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ragul-tickey/devlopment.git'
            }
        }
        stage('Build') {
            steps {
                sh 'npm install' // or any other build commands you have
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh 'ls -la' // List files in current directory
                    sh 'ls -la /var/www/html' // List files in /var/www/html
                    sh 'sudo rm -rf /var/www/html/*' // Remove existing files in /var/www/html
                    sh 'sudo cp -r * /var/www/html' // Copy files to /var/www/html
                    sh 'ls -la /var/www/html' // List files in /var/www/html after deployment
                }
            }
        }
    }
}
