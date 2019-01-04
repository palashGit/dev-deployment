//Testing CD pipeline new change 
//Testing CD1 pipeline new change 
#!/usr/bin/env groovy

pipeline {
    agent any  
    stages {
         stage('Nexus Login') { 
            steps { 
                sh 'docker login ec2-3-85-25-223.compute-1.amazonaws.com:8083'
               }
        }
        stage('Image pull') { 
            steps { 
                sh 'docker pull ec2-3-85-25-223.compute-1.amazonaws.com:8083/redis-server:latest' 
               }
        }
         stage('Docker Run') { 
            steps { 
               sh 'docker run -itd -p 6379 ec2-3-85-25-223.compute-1.amazonaws.com:8083/redis-server:latest'
            }
        }
    }
}
