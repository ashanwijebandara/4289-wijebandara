
pipeline {
    agent any
    stages {
        stage('Checkout git branch') {
            steps {
                checkout scm
            }
        }
        stage('Run Docker Compose') {
            steps {
                bat 'docker compose up'
            }
        }
    }
}