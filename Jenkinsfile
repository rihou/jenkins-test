pipeline {
        agent any
        parameters {
            string(name: 'custom_var', defaultValue: '')
        }

     stages {
        stage("make param global") {
             steps {
               sh 'tmp_param =  sh (script: 'most amazing shell command', returnStdout: true).trim()'
               sh 'env.custom_var = tmp_param' 
              }
        }
        stage("test if param was saved") {
            steps {
              echo "${env.custom_var}"
            }
        }
     }
}