pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                checkout scm
            }
        }
        stage('Run script') {
            steps{
                sh '''
                    hostname
                '''
            }
        }
    }
}
