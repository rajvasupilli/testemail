node {
    stage('Send Email') {
         mail bcc: "manidharr@gmail.com",
         //body: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]\n More info at: ${env.BUILD_URL}'",
         body: "../../jobs/${env.JOB_NAME}/builds/${env.BUILD_NUMBER}/log",
         cc: '', from: 'buildadmin', 
         replyTo: '', 
         subject: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
         to: 'raj.vasupilli@gmail.com'
    }
}

