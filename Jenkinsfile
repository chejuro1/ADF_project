

pipeline {
    agent any

     parameters {
        gitParameter name: 'TAG', 
                     type: 'PT_TAG',
                     defaultValue: 'Python'
    }

    stages {
         stage('Example') {
            steps {
                checkout([$class: 'GitSCM', 
                          branches: [[name: "${params.TAG}"]], 
                          doGenerateSubmoduleConfigurations: false, 
                          extensions: [], 
                          gitTool: 'Default', 
                          submoduleCfg: [], 
                          userRemoteConfigs: [[url: 'https://github.com/chejuro1/ADF_project.git']]
                        ])
            }
        }
    





        stage('Build') {
            steps {


                // sh  ' pip uninstall -y $(pip freeze | grep azure)'
                // sh 'pip install azure-mgmt-datafactory'
                // sh ' pip install azure-mgmt-resource'
                sh 'pip3 list | grep azure'
                sh 'python3 test.py'
            }
        }
        stage('Python') {
            // agent { docker { image 'python:3.5.1' } }
            steps {
                sh 'python3 --version'
            }

        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
