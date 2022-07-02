pipeline {
    agent any
    // tools {nodejs "node"}
    tools {nodejs "nodejs"}
    stages {
        stage('Git Setup') {
            steps {
                git branch: 'main', changelog: false, credentialsId: 'gitCredential', url: 'https://github.com/NebihaAmir/techworld-js-docker-demo-app'
              
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
      stage('Build Docker Img') {
            steps {

                sh 'docker build -t nebihaamir123/my-nodejs-app:1.3'                
               
            }
       }

    }
}
