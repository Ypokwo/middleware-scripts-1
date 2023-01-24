pipeline {
    agent any

    stages{
        stage("create zip file"){
            steps{
               
           sh 'zip mdwScript-$(date +%d%m%y-%H%M%S).zip *  --exclude Jenkinsfile README.md '  
            
            }
        }
       
        stage('Slack') {
            steps {
                slackSend color: 'good', message: 'All files has been zipped successfully'
            }
        }

     }
  }

