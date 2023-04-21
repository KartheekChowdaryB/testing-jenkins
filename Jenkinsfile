#!groovy

pipeline {
	agent none
  stages {
    stage('Docker Build') {
    	agent any
      steps {
      	sh 'docker build -t vistannextgenhyd/ros2:testing .'
      }
    }
    stage('login') {
    	agent any
      steps {
      	sh 'docker login -u "vistanNextGenHyd" -p "V!5t@n@12345**" docker.io'
      }
    }
    stage('Push image') {
        withDockerRegistry([ credentialsId: "DockerHub Credentials", url: "" ]) {
        sh "docker push vistannextgenhyd/ros2:testing"
        }
  }
}
