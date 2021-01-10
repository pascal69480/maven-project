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
            post {
                success {
                    echo 'Now Archiving...'
                }
                failure { echo 'error on the build steps !!!'}
            }
        }
    }
}