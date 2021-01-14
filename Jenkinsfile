pipeline {
    agent any
    parameters {
            string(defaultValue: "Maintainer", description: 'Enter User Role', name: 'userRole')
    }
    stages {
        stage('listVals') {
            steps {
                echo "user role = ${prams.useRole}"
                
            }
            post{
                success {
                    echo "stage listVals is OK"
                }
                failure {
                   echo "Prob in this stage"
                }
            }
                

        }
            

        }

    }