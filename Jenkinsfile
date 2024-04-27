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
                    sh 'rm -rf /var/www/html/*' // Clear existing files in /var/www/html
                    sh 'cp -r . /var/www/html' // Copy files to /var/www/html
                }
            }
        }
    }
}
