

pipeline {
    agent any

    stages {
        stage('Build') {

            steps {
                script{
                
                     env.Moar = "maor wasihon"
                }
                sh 'dotnet build' 
                sh '$env.Maor'
                  
            }
        }
        
        stage('deploy') {
            steps {

                
                  
            }
        }
            
     }
    
}
