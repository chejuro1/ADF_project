

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'pip install azure-mgmt-datafactory'
                sh ' pip install azure-mgmt-resource'
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
