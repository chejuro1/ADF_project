pipeline {
  agent {
      label "ADF"
  }
    environment {
       
      serviceADF = credentials('serviceADF')
      //$tenantID = credentials('jenkins-aws-secret-key-id')
       //$appId = credentials('jenkins-aws-secret-key-id')
       //$clientSecrets = credentials('jenkins-aws-secret-key-id')
       //$subscriptionId = "<your subscription ID to create the factory>"
       //$resourceGroupName = "<your resource group to create the factory>"
       //$factoryName = "<specify the name of data factory to create. It must be globally unique.>"
       //$apiVersion = "2018-06-01"
    }
  
  stages {
    stage('AZ connection) {
      steps {
         withCredentials([azureServicePrincipal('serviceADF')]) {
  sh 'az login --service-principal -u $AZURE_CLIENT_ID -p $AZURE_CLIENT_SECRET -t $AZURE_TENANT_ID'
}
}
        
        
        sh 'az account list'
      }
    }
  }
}
