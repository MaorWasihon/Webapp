        
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
        
        stage('deploy'){ 
        
        
          
        }//deploy
        
        
     }//stages
    
}//pipeline
