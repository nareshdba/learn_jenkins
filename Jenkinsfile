pipeline {
    agent {
        label 'agent1'
    }
    options {
        timeout(time: 100, unit: 'SECONDS')
        disableConcurrentBuilds()
            }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
        stage('print params') {
            steps {
                echo "Hello ${params.PERSON}"
                echo "Biography: ${params.BIOGRAPHY}"
                echo "Toggle: ${params.TOGGLE}"
                echo "Choice: ${params.CHOICE}"
                echo "Password: ${params.PASSWORD}"
                echo "github trigger again"
            } 
        }
    }
}