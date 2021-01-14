pipeline {
    agent any
    parameters {
            string(defaultValue: "Maintainer", description: 'Enter User Role', userRole)
    }
    stages {
        stage('listVals') {
            steps {
                echo "user role = ${params.userRole}"
                post {
                    success {
                        echo " User identified"
                    }
                    failure {
                        echo 'Build failed'
                
                    }
                    
                }
            }

        }
            

        }

    }