pipeline {  
    agent {label 'nova'}
   
    stages {
        stage ("deploying"){
            steps{                     
                sh 'cd /home/nova/beautinova-backend'
                sh 'sudo pkill node'
                sh 'supervisorctl restart beautinova-api'
                sh 'sudo pkill node'           
                echo 'test the deploying......'    
                
            }
        }
    }
}
