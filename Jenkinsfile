pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh 'echo "$JENKINS_HOME"'
                sh 'echo "$BUILD_ID"'
                sh 'echo "name=$name"'
                sh 'action=start'
                sh 'echo "action=$action"'
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