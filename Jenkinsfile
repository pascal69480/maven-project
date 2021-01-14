pipeline {
    agent any
    //triggers {
        // pollSCM('3 * * * *')
   // }
    stages{
        stage('Build'){
            steps {
                // ajout d'une liste de choix
                def choice = input message: 'choisir dans la liste',
                 parameters: [choice(choices:"choix1\nchoix2\nchoix3\n",
                 description: 'choose an option', name: 'Options')]
                sh 'echo build stage'
            }
        }    
        stage('deploy'){
            steps {
                input message:'Approve PRODUCTION Deployment?', ok: 'Yes', submitter: 'admin'
                sh 'echo deploy to tomcat server'
            }
            post {
            success {
                echo 'Code deployed to Production.'
                echo "active user is now ${params.USERID}"
                }
            }
        
            
    }
        
        }
}