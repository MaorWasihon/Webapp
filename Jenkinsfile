
  def resourceGroup = 'maor'
        
pipeline {
    agent any

    
    
    stages {
        stage('Build') {

            steps {
               
                sh 'dotnet build'        
            
            }
        }//build
        
        stage('deploy'){ 
        
          sh 'echo resourceGroup'
        }//deploy
        
        
     }//stages
    
}//pipeline
