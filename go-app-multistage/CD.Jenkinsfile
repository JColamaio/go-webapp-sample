pipeline {
    agent any
    tools {
        go 'go-1.17'
    }

    environment {
        GO111MODULE='on'
    }

    stages {
        stage {
            git 'git@github.com:JColamaio/go-webapp-sample.git'
        }
    }
        stage {
            "Building our image" {
                steps {
                    script {
                        app = docker.build("JColamaio/go-webapp-sample")
                    }
                }
            }
        }
}