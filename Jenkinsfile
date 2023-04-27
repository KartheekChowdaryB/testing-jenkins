#!groovy

pipeline {
	agent none
  stages {
  	stage('docker Install') {
    	agent {
      	docker {
        	image 'ubuntu:20.04'
        }
      }
      steps {
      	echo 'done'
      }
    }
    stage('Docker Build') {
    	agent any
      steps {
      	sh 'docker build -t ubuntu:latest .'
      }
    }
  }
}
