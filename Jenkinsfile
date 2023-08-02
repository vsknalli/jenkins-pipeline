node {
  stage('SCM Chekcout'){
    git 'https://github.com/vsknalli/jenkins-pipeline'    
  }
  stage('Compile & packae'){
    // get maven hoem path
    def mavenhome = tool name: 'maven-3', type: 'maven'
    sh "${mavenhome}/bin/mvn package"
  }
  stage('Slack Notification'){
       slackSend baseUrl: 'https://hooks.slack.com/services/', 
       channel: '#jenkinspipeline', 
       color: 'good', 
       message: 'Welcome to jenkins Slack!', 
       tokenCredentialId: 'slack'
  }
   
}


