#!/usr/bin/env groovy
properties([pipelineTriggers([githubPush()])])
//comment testing
pipeline {
    agent any 

    stages {
        stage('Build') { 
            steps { 
                sh 'pwd' 
            }
        }
        stage('Test'){
            steps {
                sh 'java -version'
                
            }
        }
        stage('Deploy') {
            steps {
                sh 'ls'
            }
        }
    }
}
