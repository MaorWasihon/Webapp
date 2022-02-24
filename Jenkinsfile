import groovy.json.JsonSlurper      
pipeline {
    agent any
 
  
    environment {
        
        CLIENT_ID = "5b7b0709-2444-4691-90a2-ca9b343605c4"
        CLIENT_SECRET_ID ="OqWWHbkHwrZX~f-JI6ZV93W2Cu5Pfgv~wn"
        TENANT_ID = "b5f3202f-73b3-40a8-a61e-596ab18836ea"
        SUBSCRIPTION_ID = "dc2bcd48-29b9-4103-9467-4cb230777959"
        RESOURCE_GROUP = "jenkins-get-started-rg"
        WEB_APP_NAME = "my-app-now"
       
    }
        
        
    stages {
        stage('Build') {

            steps {
               
                sh 'dotnet build'   
                sh 'echo CLIENT_ID ${CLIENT_ID}'
                    sh 'echo CLIENT_SECRET_ID ${CLIENT_SECRET_ID}'
                    sh 'echo SUBSCRIPTION_ID  ${SUBSCRIPTION_ID}'
                    sh 'echo RESOURCE_GROUP   ${RESOURCE_GROUP}'
                    sh 'echo WEB_APP_NAME   ${WEB_APP_NAME}'
            
            }
         }//build
            
        
        stage('deploy'){
            
            steps{
                sh ''' 
                    az login --service-principal -u ${CLIENT_ID} -p ${CLIENT_SECRET_ID} -t ${TENANT_ID}
                '''
            }
            
        }//deploy
            
     
            
            
            
       
     }//stages
    
}//pipeline
