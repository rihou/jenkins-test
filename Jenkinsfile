pipeline {
    agent any

    environment {
        packageName='my-package'
    }

    stages {
        stage('first stage') {
            steps {
                // write out any env vars you like to a temp file
                sh 'env.packageName=my-package-1'

            }
        }
        stage ("later stage") {
            steps { 
                sh 'echo ${env.packageName}'
            }

        }
     }

}