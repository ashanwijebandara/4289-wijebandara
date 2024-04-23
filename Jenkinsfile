pipeline {
  agent any
  triggers{
    githubPush()
  }
  stages {
    stage('Docker Build'){
      steps {
        bat 'docker build -t ashanwijebandara/4289-wijebandara .'
      }
    }
    stage('Docker Run'){
      steps{
        bat 'docker run -d -p 3001:3001 ashanwijebandara/4289-wijebandara'
      }
    }
    stage('Final'){
      steps{
        bat 'docker ps'
      }
    }}
}