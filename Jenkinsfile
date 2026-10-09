pipeline {
    agent any
    triggers {
        pollSCM('H/2 * * * *')
    }
    stages {
        stage('Hello') {
            steps {
                echo 'hello from github'
            }
        }
        stage('Files') {
            steps {
                sh 'ls -l'
            }
        }
        stage('Commit') {
            steps {
                sh 'git log --oneline -3'
            }
        }
    }
}
