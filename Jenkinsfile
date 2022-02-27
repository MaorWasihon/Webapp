

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {

               sh '''
                    dotnet build -c Release
                    dotnet publish -c Release --no-build
                  '''
                  
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
