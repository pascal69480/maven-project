pipeline {
    agent any
    triggers {
         pollSCM('* * * * *')
    stages{
        stage('Build'){
            steps {
                sh 'mvn validate clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
                failure { echo 'error on the build steps !!!'}
            }
        }
    }
}