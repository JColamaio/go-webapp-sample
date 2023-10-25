pipeline {
    agent {
        docker { image 'golang:latest'}
    }

    stages {
        stage('Development') {
            steps {
                git 'git@github.com:JColamaio/go-webapp-sample.git'
                sh 'go version'
            }
        }
    }
}