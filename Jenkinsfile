pipeline {
    agent {
        label 'agent1'
    }
    options {
                // Timeout counter starts BEFORE agent is allocated
        timeout(time: 1, unit: 'SECONDS')
            }
    stages {
        stage('Build') {
            steps {
                sh 'echo build the project'
            }
        }
        stage('Test') {
            steps {
                sh 'echo test the project'
                sh 'sleep 10'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo deploy the project'
            }
        }
    }
}