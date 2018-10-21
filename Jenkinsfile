pipeline {
    agent any

    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }

    stages {
        stage('Build') {
            steps {
                sh 'echo "$DB_ENGINE"'
                sh 'DB_ENGINE=test'
                sh 'echo "$DB_ENGINE"'
            }
        }
    }
}