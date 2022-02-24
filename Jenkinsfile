

pipeline {
    agent any

    stages {
        stage('Build') {
            script{
                
                env.Moar = "maor wasihon"
            }
            steps {

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
