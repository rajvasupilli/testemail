pipeline {
 agent any

  stages {
stage('Checkout SCM') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'raju', url: 'https://github.com/rajvasupilli/testemail.git']]])
            }
        }
 }
 post {
 success {
 sendEmail("Successful")
 }
 failure {
 sendEmail("Failed")
 }
 }
}

@NonCPS
def getChangeString() {
 MAX_MSG_LEN = 100
 def changeString = ""

 echo "Gathering SCM changes"
 def changeLogSets = currentBuild.changeSets
 for (int i = 0; i < changeLogSets.size(); i++) {
 def entries = changeLogSets[i].items
 for (int j = 0; j < entries.length; j++) {
 def entry = entries[j]
 truncated_msg = entry.msg.take(MAX_MSG_LEN)
 
 changeString += " ${entry.commitId} by ${entry.author} on ${new Date(entry.timestamp)}: ${entry.msg}\n"     
 }
 }

 if (!changeString) {
 changeString = " - No new changes"
 }
 return changeString
}

def sendEmail(status) {
 mail (
 to: "raj.vasupilli@gmail.com",
 subject: "Build $BUILD_NUMBER - " + status + " ($JOB_NAME)",
 body: "Changes:\n " + getChangeString() + "\n\n Check console output at: $BUILD_URL/console" + "\n")
}

	
	
	
