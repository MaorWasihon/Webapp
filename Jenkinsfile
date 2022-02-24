        
pipeline {
    agent any
 
  
    environment {
        MAOR = "maor"
    }
    stages {
        stage('Build') {

            steps {
               
                sh 'dotnet build'   
                sh 'echo ${MAOR}'
            
            }
        }//build
       
     }//stages
    
}//pipeline
