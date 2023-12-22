#!/usr/bin/env groovy

pipeline {
    agent any
    stages {
        stage('build app') {
            steps {
               script {
                   echo "building the application..."
               }
            }
        }
        stage('build image') {
            steps {
                script {
                    echo "building the docker image..."
                }
            }
        }
        stage('deploy') {
            environment {
               AWS_ACCESS_KEY_ID = credentials('Jenkins-AWS-ACCESS-KEY')
               AWS_SECRET_ACCESS_KEY = credentials('Jenkins-AWS-SECRET-ACCESS-KEY')
            }
            steps {
                script {
                   echo 'deploying docker image....'
                   sh 'kubectl create deployment nginx-deployment --image=nginx'
                }
            }
        }
    }
}
