node {
    agent any
       stage('build') {
            steps {
                sh 'echo "Test Email Functionality!!!"'
            }
        }
    
    post {
        success {
      emailext (
          to: 'raj.vasupilli@gmail.com',
          subject: "SUCCESSFUL: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
          body: """<p>SUCCESSFUL: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]':</p>
            <p>Check console output at &QUOT;<a href='${env.BUILD_URL}'>${env.JOB_NAME} [${env.BUILD_NUMBER}]</a>&QUOT;</p>""",
          recipientProviders: [[$class: 'DevelopersRecipientProvider']]
        )
        }
    }

}
