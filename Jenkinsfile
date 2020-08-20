pipeline {
    agent any
    

    stages {
        stage ('build locally'){
            steps{
                echo 'hello'
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
