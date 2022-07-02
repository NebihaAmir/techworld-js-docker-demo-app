pipeline {
    agent any
    // tools {nodejs "node"}
    environment {
        ENV_NAME = "${PATH}"
    }
    tools {nodejs "nodejs"}
    stages {
        stage('Git Setup') {
            steps {
                git branch: 'main', changelog: false, credentialsId: 'gitCredential', url: 'https://github.com/NebihaAmir/techworld-js-docker-demo-app'
              
            }
        }
            stage('Build Docker Img') {
                steps {

                    sh 'docker build -t nebihaamir123/my-nodejs-app:1.3'                
                
                }
        }
            stage('Initialization') {
                steps {
                    dir('app') {
                        sh 'npm install express'
                        sh 'npm start'
                        }                   
                
                }
       }
    //    building docker img


    }
}
