pipeline {
    agent any

    stages {
        stage ('Deploy To Dev'){
            steps{
                echo 'Stage 1'
            }
        }
        
        stage ('Deploy to QA'){
            steps {
                 echo 'Stage 2!!!'
                  sh exit (1)
                }
            }
        
         stage ('Deploy To Prod'){
            steps{
                echo 'Stage 3!!!'
            }
        }
    }
    
 }

