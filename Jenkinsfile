pipeline {
    agent any
    parameters {
            string(defaultValue: "Maintainer", description: 'Enter User Role')
    }
    stages {
        stage('listVals')
            steps {
                echo "user's role = ${params.userRole}"
                post {
                    success {
                        echo " User identified"
                    }
                    failure {
                        echo 'Build failed'
                        mail body : "le job ${CURRENT_JOB_ID} is considered failed", subject: 'job failed!',
                        to: 'imejri.issam@gmail.com'
                    }
                    
                }
            }

        }

    }