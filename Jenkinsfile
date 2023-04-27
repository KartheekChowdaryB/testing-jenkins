#!groovy

pipeline {
    agent any

    stages {
        stage('Build') {
            agent any
                
            steps {
                sh 'docker pull ubuntu:20:04'
                
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
