pipeline {
    agent any
    environment {
      //  SERVER_CREDENTIALS = credentials('nova-credentials')
    } 
    stages {
        stage ("deploying"){
            steps{              
                sh 'sudo cd /home/nova/beautinova-backend'
                sh 'sudo pkill node'
                sh 'sudo supervisorctl restart beautinova-api'
                sh "sudo pkill node"
                withCredentials ([
                    usernamePassword(credentials:'nova-credentials', usernameVariable:USER, passwordVariable: PWD)
                ]) {
                    sh "some script ${USER} ${PWD}"
                }
            }
        }
    }
}