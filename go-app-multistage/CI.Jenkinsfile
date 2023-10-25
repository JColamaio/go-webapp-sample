pipeline {
    agent any
    tools {
        go 'go-1.17'
    }
    environment {
        GO111MODULE='on'
    }
// CI
    stages {
        stage('Test') {
            steps {
                // get some code from GitHub
                git 'git@github.com:JColamaio/go-webapp-sample.git'
                sh 'go test ./...'
            }
        }
    }
        stage('UAT') {
            steps {
                // Get some code from Github
            git 'git@github.com:JColamaio/go-webapp-sample.git'
            }
        }
}