pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'npm i -save express' 
                sh 'make'
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
            }
        }
        stage('Test') {
           steps {
                sh 'npm test'
           }
        }
    }
}    