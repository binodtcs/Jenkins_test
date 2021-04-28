pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Hello World'
                git changelog: false, credentialsId: '9c5b4b7f-1875-4d1a-a843-02508a8fc94b', poll: false, url: 'https://github.com/binodtcs/Jenkins_test.git'
            }
        }
        stage('Hello2'){
            steps{
                echo 'My first pipeline'
            }
        }
        
    }
        post {
         success {
           mail to: 'binod.chowdhury@ah.nl',
           subject: "Pipeline has failed: ${currentBuild.fullDisplayName}",
            body: "Error in ${env.BUILD_URL}"
          }
        }
    
}
