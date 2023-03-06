#!/usr/bin/env groovy

pipeline {

    agent {
        triggers {
    githubPush()
  }
        docker {
            image 'node'
            args '-u root'
        }
    }  
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'npm test'
            }
        }
    }
}

