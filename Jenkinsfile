

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {

               sh 'dotnet build'
                  
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
