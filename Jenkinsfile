

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'pwd'
                sh 'ls'
                sh 'pip3 list | grep azure'
                sh 'python3 test.py'
            }
        }
        stage('Python') {
            // agent { docker { image 'python:3.5.1' } }
            steps {
                sh 'python --version'
            }

        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
