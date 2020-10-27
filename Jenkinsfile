

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'pwd'
                sh 'ls'
                sh 'python3 --version'
            }
        }
        stage('Python') {
            agent { docker { image 'python:3.5.1' } }
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
