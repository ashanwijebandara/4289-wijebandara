pipeline {
    agent any
    
    environment {
        GITHUB_REPO_URL = 'https://github.com/ashanwijebandara/4289-wijebandara.git'
    }
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: "${env.GITHUB_REPO_URL}"
            }
        }
        
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t app-backend .'
            }
        }
        
        stage('Run Docker Image') {
            steps {
                bat 'docker run -d -p 3001:3001 app-backend'
            }
        }
        
    }
}