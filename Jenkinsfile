node {
    //checkout git 'https://github.com/reiseburo/hermann.git'
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'raju', url: 'git@github.com:rajvasupilli/testemail.git']]])
    stage('Send Email') {
         emailext attachLog: true, body:
   """<p>EXECUTED: Job <b>\'${env.JOB_NAME}:${env.BUILD_NUMBER})\'
   </b></p><p>View console output at "<a href="${env.BUILD_URL}">
   ${env.JOB_NAME}:${env.BUILD_NUMBER}</a>"</p>
     <p><i>(Build log is attached.)</i></p>""",
    compressLog: true,
    recipientProviders: [[$class: 'CulpritsRecipientProvider'],
 [$class: 'DevelopersRecipientProvider'],
 [$class: 'RequesterRecipientProvider'],
 [$class: 'FailingTestSuspectsRecipientProvider'],
 [$class: 'FirstFailingBuildSuspectsRecipientProvider'],
 [$class: 'UpstreamComitterRecipientProvider']],
    replyTo: 'do-not-reply@company.com',
    subject: "Build Status: ${currentBuild.currentResult} - Job '${env.JOB_NAME} [${env.BUILD_NUMBER}]'",
    to: 'raj.vasupilli@gmail.com'
    }
}
