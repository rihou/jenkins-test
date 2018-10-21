pipeline {
        agent any
        parameters {
            string(name: 'custom_var', defaultValue: '')
        }

     stages {
        stage("make param global") {
             steps {
               
               sh 'env.custom_var = "tmp_param"' 
              }
        }
        stage("test if param was saved") {
            steps {
              echo "${env.custom_var}"
            }
        }
     }
}