pipeline {
    agent any
    triggers {
         pollSCM('* * * * *')
    }
    stages{
        stage('Build'){
            steps {
                sh 'echo build stage'
            }
        stage('deploy')
            steps {
                input message:'Approve PRODUCTION Deployment?'
                sh 'echo deploy to tomcat server'
            }
            post {
                success {
                    echo 'Now Archiving...'
                }
                failure { echo 'error on the build steps !!!'}
            }
        }
    }
}