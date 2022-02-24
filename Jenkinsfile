pipeline {
    agent any

    stages {
        stage('Build') {
            steps {

               sh 'sudo dotnet run'
                  
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
