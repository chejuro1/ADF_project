pipeline {
  agent {
      label "ADF"
  }
    environment {
       
      
      
       //$appId = credentials('jenkins-aws-secret-key-id')
       //$clientSecrets = credentials('jenkins-aws-secret-key-id')
       subscriptionId = "7dc654d6-8566-4e2f-a781-1eadeb4e7734"
       resourceGroupName = "test"
       factoryName = "adfchejurotest"
       apiVersion = "2018-06-01"
   }
  
  stages {
    stage('AZ connection') {
      steps {
        withCredentials([azureServicePrincipal('serviceADF1')]) {
          
          
          sh 'az login --service-principal -u $AZURE_CLIENT_ID -p $AZURE_CLIENT_SECRET -t $AZURE_TENANT_ID'
           }
         
      
        
        
        sh 'az account list'
      }
      
    }
    stage('pwsh') {
       // agent {
    //docker {
       //image 'ubuntu'
       // label 'pwsh'
        //args  '-v /tmp:/tmp'
        //  }
    // }
      
      steps{
         
        echo 'helow-world'
                 
              
         
         
            }
          }

  }
}

