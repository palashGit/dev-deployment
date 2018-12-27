#!/usr/bin/env groovy

pipeline {
    agent any  
    stages {
         stage('Nexus Login') { 
            steps { 
                sh 'docker login ec2-54-173-108-195.compute-1.amazonaws.com:8083'
               }
        }
        stage('Image pull') { 
            steps { 
                sh 'docker pull ec2-54-173-108-195.compute-1.amazonaws.com:8083/nginx-server:latest' 
               }
        }
         stage('Docker Run') { 
            steps { 
               sh 'docker run -itd -p 443 ec2-54-173-108-195.compute-1.amazonaws.com:8083/nginx-server:latest'
            }
        }
    }
}
