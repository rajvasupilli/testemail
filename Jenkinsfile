node {
    stage('Send Email') {
        
       // emailext attachLog: true, body: "${currentBuild.result}: ${BUILD_URL}", compressLog: true, replyTo: 'raj.vasupilli@gmail.com',
        emailext attachLog: true,
     body: "${currentBuild.currentResult}: Job ${env.JOB_NAME} build ${env.BUILD_NUMBER}\n More info at: ${env.BUILD_URL}",
     recipientProviders: [developers(), requestor()],
     subject: "Jenkins Build ${currentBuild.currentResult}: Job ${env.JOB_NAME}",
     to: 'raj.vasupilli@gmail.com'
       
        //subject: "Build Notification: ${JOB_NAME}-Build# ${BUILD_NUMBER} ${currentBuild.result}", to: 'raj.vasupilli@gmail.com'        

                 //attachmentsPattern: '../../jobs/${env.JOB_NAME}/builds/${env.BUILD_NUMBER}/log'        
    }
}

