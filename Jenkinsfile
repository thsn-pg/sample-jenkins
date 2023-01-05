pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: env.GIT_REPOSITORY]]])
            }
        }
        stage('Build') {
            steps {
                sh "echo build"
            }
        }
        stage('Test') {
            steps {
                sh "echo test"
            }
        }
        stage('Deploy') {
            steps {
                sh "echo deploy"
            }
        }
    }
}