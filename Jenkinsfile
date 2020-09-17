node {
    stage('Send Email') {
        emailext attachLog: true, attachmentsPattern: '$JENKINS_HOME/jobs/$JOB_NAME/builds/$BUILD_NUMBER/log',
         //mail bcc: "manidharr@gmail.com",
         body: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]\n More info at: ${env.BUILD_URL}'",
         //body: "Check the log: $JENKINS_HOME/jobs/$JOB_NAME/builds/$BUILD_NUMBER/log",
         //cc: "manidharr@gmail.com", 
         from: 'buildadmin', 
         replyTo: 'raj.vasupilli@gmail.com', 
         subject: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
         to: 'raj.vasupilli@gmail.com'
    }
}
    
