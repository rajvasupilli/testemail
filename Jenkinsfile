node {
    stage('Send Email') {
        
        emailext attachLog: true, body: "${currentBuild.result}: ${BUILD_URL}", compressLog: true, replyTo: 'raj.vasupilli@gmail.com',
        subject: "Build Notification: ${JOB_NAME}-Build# ${BUILD_NUMBER} ${currentBuild.result}", to: 'raj.vasupilli@gmail.com'        

                 //attachmentsPattern: '../../jobs/${env.JOB_NAME}/builds/${env.BUILD_NUMBER}/log'
         //emailext attachLog: true, body: "${currentBuild.result}: ${BUILD_URL}/log", compressLog: true, replyTo: 'raj.vasupilli@gmail.com',
       //subject: "Build Notification: ${JOB_NAME}-Build# ${BUILD_NUMBER} ${currentBuild.result}", to: 'raj.vasupilli@gmail.com'
         
    }
}

