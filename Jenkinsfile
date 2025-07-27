pipeline {
    agent any
    environment {
        IMAGE_NAME = 'greeting-app'
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/TirthankarSingh/greeting-app.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    bat 'docker build -t $IMAGE_NAME .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    bat 'docker run --rm $IMAGE_NAME'
                }
            }
        }
    }
}
