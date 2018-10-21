#!/usr/bin/env groovy
pipeline {
    agent any

    environment {
        packageName='my-package'
    }

    stages {
        stage('first stage') {
            steps {
                // write out any env vars you like to a temp file
                script {
                packageName = 'my-package-1'
                env.packageName = packageName
            }

            }
        }
        stage ("later stage") {
            steps { 
                script {
                    echo "${packageName}"
                    echo "${env.packageName}"

                } 

                sh 'echo "${packageName}"'
            }

        }
     }

}