node {
    stage('Send Email') {
        //emailext attachLog: true, attachmentsPattern: 'builds/$BUILD_NUMBER/log',
         mail bcc: "manidharr@gmail.com",
         body: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]\n More info at: ${env.BUILD_URL}'",
         //body: "Check the log: builds/$BUILD_NUMBER/log",
         cc: '', from: 'buildadmin', 
         replyTo: '', 
         subject: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
         to: 'raj.vasupilli@gmail.com'        
    }
}
    
