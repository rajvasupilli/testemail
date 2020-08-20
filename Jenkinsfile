pipeline {
    agent any

    stages {
        stage ('Deploy To Dev'){
            steps{
                echo 'The next stage would test the manual approval process!!!'
            }
        }
        
        stage ('Prompt check'){
            steps {
            mail to: 'raj.vasupilli@gmail.com',
                 cc : 'manidharr@gamil.com'
                subject: "INPUT: Build ${env.JOB_NAME}", 
                body: "Awaiting for your input ${env.JOB_NAME} build no: ${env.BUILD_NUMBER} .Click below to promote to production\n${env.JENKINS_URL}job/${env.JOB_NAME}\n\nView the log at:\n ${env.BUILD_URL}\n\nBlue Ocean:\n${env.RUN_DISPLAY_URL}"
                timeout(time: 60, unit: 'MINUTES'){
                    input message: "Promote to Production?", ok: "Promote"
                }
            }
        }
    }
}
