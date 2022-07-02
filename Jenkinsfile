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
        stage('initialization') {
            steps {
                dir('app') {
                    sh 'npm install express'
                    sh 'npm start'
                    }                   
               
            }
       }

    }
}
