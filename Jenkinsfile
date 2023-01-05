pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: env.GIT_REPOSITORY]]])
            }
        }
        stage('Build') {
            steps {
                // Run your build steps here
            }
        }
        stage('Test') {
            steps {
                // Run your tests here
            }
        }
        stage('Deploy') {
            steps {
                // Deploy your application
            }
        }
    }
}