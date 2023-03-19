pipeline {
    agent any 
    stages {
        stage('cloning') { 
            steps {
                git branch: 'main', credentialsId: '1', url: 'https://github.com/aditya10mm/html-website.git' 
            }
        }
        stage('deploying') { 
            steps {
                sh 'ls'
                sh 'pwd'
                sh 'ssh -o StrictHostKeyChecking=no root@172.21.242.50'
                sh 'scp -r $(pwd)/* root@172.21.242.50:/home'
                
            }
        }        
    }
}
