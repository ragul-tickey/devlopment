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
                sh 'cp -r * /var/www/html' // Assuming your build outputs to current directory
            }
        }
    }
}
