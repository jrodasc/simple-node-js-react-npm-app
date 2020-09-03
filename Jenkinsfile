pipeline {
    agent 
     {
         docker
          {
            image 'maven:3-alpine'
            //This exposes application through port 8081 to outside world
            args '-u root -p 8081:8081 -v /var/run/docker.sock:/var/run/docker.sock  '
         }
    } 
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
    }
}