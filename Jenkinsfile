node {
    stage('Send Email') {
       mail attachLog: true,
       body: "${currentBuild.result}: ${BUILD_URL}/log",
       compressLog: true,    
       bcc: "manidharr@gmail.com",
         //body: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]\n More info at: ${env.BUILD_URL}'",
         //body: "",
         cc: '', from: 'buildadmin', 
         replyTo: '', 
         subject: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
         to: 'raj.vasupilli@gmail.com'
         //attachmentsPattern: '../../jobs/${env.JOB_NAME}/builds/${env.BUILD_NUMBER}/log'
         //emailext attachLog: true, body: "${currentBuild.result}: ${BUILD_URL}/log", compressLog: true, replyTo: 'raj.vasupilli@gmail.com',
       //subject: "Build Notification: ${JOB_NAME}-Build# ${BUILD_NUMBER} ${currentBuild.result}", to: 'raj.vasupilli@gmail.com'
         
    }
}

