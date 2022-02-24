import groovy.json.JsonSlurper

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {

               sh 'dotnet msbuild -h' $(MASU)
                  
            }
        }
            
     }
    
}
