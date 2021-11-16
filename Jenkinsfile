pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'npm i -save express' 
                bat 'make'
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
            }
        }
        stage('Test') {
           steps {
                bat 'npm test'
           }
        }
    }
}    