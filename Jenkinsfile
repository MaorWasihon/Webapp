pipeline {
    agent any

    stages {
        stage('Build') {
            steps {

               sh 'dotnet run'
                  
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
                
                def resourceGroup = 'jenkins-get-started-rg'
                def webAppName = 'my-app-now'
                // login Azure
                withCredentials([usernamePassword(credentialsId: 'azure-cloud', passwordVariable: 'AZURE_CLIENT_SECRET', usernameVariable: 'AZURE_CLIENT_ID')]) {
                sh '''
                    az login --service-principal -u $AZURE_CLIENT_ID -p $AZURE_CLIENT_SECRET -t $AZURE_TENANT_ID
                    az account set -s $AZURE_SUBSCRIPTION_ID
                    '''
      }
      // get publish settings
      def pubProfilesJson = sh script: "az webapp deployment list-publishing-profiles -g $resourceGroup -n $webAppName", returnStdout: true
      def ftpProfile = getFtpPublishProfile pubProfilesJson
      // upload package
      sh "curl -T target/calculator-1.0.war $ftpProfile.url/webapps/ROOT.war -u '$ftpProfile.username:$ftpProfile.password'"
      // log out
      sh 'az logout'
            }
        }
    }
}
