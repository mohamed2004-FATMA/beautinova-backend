pipeline {
    agent any 
    stages {
        stage ("deploying"){
            steps{
                sh 'cd /home/nova/beautinova-backend'
                sh 'sudo pkill node'
                sh 'sudo supervisorctl restart beautinova-api'
                sh 'sudo pkill node'
            }
        }
    }
}