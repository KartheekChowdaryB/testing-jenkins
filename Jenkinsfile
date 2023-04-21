#!groovy

pipeline {
	agent none
  stages {
    stage('Docker Build') {
    	agent any
      steps {
      	sh 'docker build -t vistannextgenhyd/ros1:testing .'
      }
    }
    stage('Push image') {
        withDockerRegistry([ credentialsId: "DockerHub Credentials", url: "" ]) {
        sh "docker push vistannextgenhyd/ros1:testing"
        }
  }
}
