#!/usr/bin/env groovy
pipeline {
    agent any

    def content
    stages {
        stage('first stage') {
            steps {
            content = "hello"

            }
        }
        stage ("later stage") {
            steps {

                sh 'echo "${content}"'
            }

        }
     }

}