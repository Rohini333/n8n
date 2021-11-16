pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'npm'
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