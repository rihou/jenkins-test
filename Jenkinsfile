pipeline {
        parameters {
            string(name: 'custom_var', defaultValue: '')
        }

        stage("make param global") {
             steps {
               tmp_param =  sh (script: 'most amazing shell command', returnStdout: true).trim()
               env.custom_var = tmp_param 
              }
        }
        stage("test if param was saved") {
            steps {
              echo "${env.custom_var}"
            }
        }
}