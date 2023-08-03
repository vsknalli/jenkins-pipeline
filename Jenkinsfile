node {
  stage('SCM Chekcout'){
    git 'https://github.com/vsknalli/jenkins-pipeline'    
  }
  stage('Compile & packae'){
    // get maven hoem path
    def mavenhome = tool name: 'maven-3.9.3', type: 'maven'
    sh "${mavenhome}/bin/mvn package"
  }
  stage('Slack Notifications'){
    slackSend baseUrl: 'https://hooks.slack.com/services/', 
      channel: '#devopscicd', 
      color: 'good', 
      message: 'Welcome to SenthilVeeranans\'s DevOps World...!!!', 
      tokenCredentialId: 'slack'
  }
  
}


