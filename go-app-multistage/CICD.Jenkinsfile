pipeline {
    agent anytools {
        go 'go-1.17'
    }

    environment {
        GO111MODULE='on'
    }

    stages {
        stage('Test') {
            steps {
                git 'git@github.com:JColamaio/go-webapp-sample.git'
                sh 'go test ./..'            
            }
        }
        stage('Build') {
            steps {
                git 'git@github.com:JColamaio/go-webapp-sample.git'
                sh 'go build .'
            }
        }
        stage('Run') {
            steps {
                sh 'cd /var/lib/jenkins/workspace/go-full-pipeline && go-webapp-sample &'
            }
        }
    }
    
}