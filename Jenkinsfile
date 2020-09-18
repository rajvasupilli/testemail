node {
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'raju', url: 'git@github.com:rajvasupilli/testemail.git']]])
    stage('Send Email') {
         emailext attachLog: true, body:
   """EXECUTED: Job \'${env.JOB_NAME}:${env.BUILD_NUMBER})\'
   View console output at "${env.BUILD_URL}"
   ${env.JOB_NAME}:${env.BUILD_NUMBER}"
     (Build log is attached.)""",
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
