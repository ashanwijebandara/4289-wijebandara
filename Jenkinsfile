
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
                sh 'docker compose up'
            }
        }
    }
}