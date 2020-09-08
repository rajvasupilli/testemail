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
                 catchError(buildResult: 'SUCCESS', stageResult: 'UNSTABLE') {
                    sh "exit 1"
                }
            }
        }
         stage ('Deploy To Prod'){
            steps{
                echo 'Stage 3!!!'
            }
        }
    }
    
 }

