pipeline {
    agent any
    triggers {
        githubPush()
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
        stage('Next') {
            steps {
                build job: 'p1', wait: false
            }
        }
    }
}
