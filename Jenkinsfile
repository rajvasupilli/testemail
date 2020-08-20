pipeline {
    agent any

    stages {
        stage ('Deploy To Dev'){
            steps{
                echo 'The next stage would test the manual approval process!!!'
            }
        }
        
        stage ('Deploy To Prod'){
           input{
                message "Do you want to proceed for production deployment?"
           }
          steps {
                 sh 'echo "Deploy into Prod"'
          }
        }
    }
}
