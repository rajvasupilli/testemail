node {
    stage('Example') {

          mail bcc: "manidharr@gmail.com",
              body: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]\n More info at: ${env.BUILD_URL}'",
                cc: '', from: 'buildadmin', 
           replyTo: '', 
           subject: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
                to: 'manidharr@gmail.com'

    }
}
    
   // post {
     //   success {
      //emailext (
       //   to: 'raj.vasupilli@gmail.com',
        //  subject: "SUCCESSFUL: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
          //body: """<p>SUCCESSFUL: Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]':</p>
            //<p>Check console output at &QUOT;<a href='${env.BUILD_URL}'>${env.JOB_NAME} [${env.BUILD_NUMBER}]</a>&QUOT;</p>""",
          //recipientProviders: [[$class: 'DevelopersRecipientProvider']]
        //)
        //}
    //}

//}
