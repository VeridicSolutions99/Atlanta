#!/usr/bin/env groovy
///worked
properties([
    [$class: 'GithubProjectProperty',
    displayName: '',
    projectUrlStr: 'https://github.com/VeridicSolutions99/Veridic_Atlanta.git/'],
    pipelineTriggers([githubPush()])])

pipeline {
    agent any 
     parameters {
            choice(name: 'ENVIRONMENT', description: 'Used for posgress.sh and CodeDeploy deployment group.', choices: 'integration\nstaging\nprod')
            booleanParam(name: 'REBUILD_DATABASE', defaultValue: false, description: 'Should we rebuild the database?') 
            booleanParam(name: 'DEPLOY', defaultValue: false, description: 'Should we deploy the application?')
            string(name: 'branch', defaultValue: 'default', description: 'Select which branch you want to select?')
        }

    stages {
        stage('Checkout') {
            steps {
                       checkout scm
                       sh 'git clean -fdx'
                  }
        }
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
                sh 'pwd'
            }
        }
    }
}
