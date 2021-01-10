pipeline {
    agent any
    triggers {
         pollSCM('3 * * * *')
    }
    stages{
        stage('Build'){
            steps {
                sh 'echo build stage'
            }
        }    
        stage('deploy'){
            steps {
                input message:'Approve PRODUCTION Deployment?'
                sh 'echo deploy to tomcat server'
            }
        }
        post {
            success {
                echo 'Code deployed to Production.'
                }
            
        }
        
        }
}