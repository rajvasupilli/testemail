pipeline {
    agent any
    

    stages {
        stage ('build locally'){
            steps{
                echo 'hello'
            }
        }
         stage ('Prompt check'){
            steps {
            
                    input message: "Promote to Production?", ok: "Promote"
                }
            }
        }
        
    }
