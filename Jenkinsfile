pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout scm
            }
        }
        stage('Build container') {
            steps{
                sh 'echo Hello world !'
            }
        }
    }
}