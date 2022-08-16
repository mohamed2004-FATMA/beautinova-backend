pipeline {
    agent any
    environment {
        SERVER_CREDENTIALS = credentials('nova-credentials')
    } 
    stages {
        stage ("deploying"){
            steps{              
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