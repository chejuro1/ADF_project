// Using git within checkout 
pipeline {
    agent any
    parameters {
        gitParameter name: 'TAG', 
                     type: 'PT_TAG',
                     defaultValue: 'develop'
    }
    stages {
        stage('Git') {
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
    }
}
