pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: 'origin/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], 
                	userRemoteConfigs: [
						[credentialsId: Boolean.parseBoolean(env.GIT_USE_SSH_KEY) == Boolean.TRUE ?
							env.GIT_SSH_CREDENTIAL_ID : env.GIT_CREDENTIAL_ID, url: env.GIT_REPOSITORY ?: 'https://github.com/thsn-pg/sample-jenkins.git']
					]
                ])
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