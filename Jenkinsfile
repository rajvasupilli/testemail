node {
    stage('Send Email') {
        emailext attachLog: true, attachmentsPattern: '$JENKINS_HOME/jobs/$JOB_NAME/builds/$BUILD_NUMBER/log',
         //bcc: "manidharr@gmail.com",
         body: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]\n More info at: ${env.BUILD_URL}'",
         //cc: '', from: 'buildadmin', 
         replyTo: '', 
         subject: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
         to: 'raj.vasupilli@gmail.com'
    }
}
    
