        
pipeline {
    agent any
 
  
    environment {
        MAOR = "maor"
    }
    stages {
        stage('Build') {

            steps {
               
                sh 'dotnet build'        
            
            }
        }//build
        
        stage('deploy'){ 
        
          sh 'echo ${MAOR}'
          
        }//deploy
        
        
     }//stages
    
}//pipeline
