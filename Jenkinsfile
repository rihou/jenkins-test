pipeline {
    agent any

    stages {
        stage('first stage') {
            steps {
                // write out any env vars you like to a temp file
                sh 'echo export FOO=baz > myenv'

                // stash away for later use
                stash 'myenv'
            }
        }
        stage ("later stage") {
            steps {

                // unstash the temp file and apply it
                unstash 'myenv'
                sh 'source ./myenv'

                // now continue on with variables set 
                sh 'echo $FOO'
            }

        }
     }

}