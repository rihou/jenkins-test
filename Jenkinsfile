pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh 'exit 1'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
                print "World----"
            }
        }
    }
}