pipeline {
  agent any
  label 'master'
  
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  environment {
    DOCKERHUB_CREDENTIALS = credentials('dockerhub')
  }
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t lloydmatereke/jenkins-docker-hub .'
      }
    }
  }
}
