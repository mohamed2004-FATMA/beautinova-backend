pipeline {
    agent any
    environment {
        SERVER_CREDENTIALS = credentials('nova-credentials')
    } 
    stages {
        stage ("deploying"){
            steps{   
                sh 'cd /home/nova/beautinova-backend'
                sh 'sudo pkill node'
                sh 'supervisorctl restart beautinova-api'
                sh 'sudo pkill node'           
                echo 'test the deploying......'
                withCredentials ([
                    usernamePassword(credentials:'nova-credentials', usernameVariable:USER, passwordVariable: PWD)
                ]) {
                    sh "some script ${USER} ${PWD}"
                }
            }
        }
    }
}