#!groovy

pipeline {
    agent any

    stages {
        stage('Build') {
            agent docker
                
            steps {
                sh 'docker build .'
                
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
