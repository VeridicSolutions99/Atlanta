#!/usr/bin/env groovy

properties([
    [$class: 'GithubProjectProperty',
    displayName: '',
    projectUrlStr: 'https://github.com/VeridicSolutions99/Veridic_Atlanta.git/'],
    pipelineTriggers([githubPush()])
])
//comment testing edited lines
//underline do
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
