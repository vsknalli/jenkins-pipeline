node{
  stage('SCM Checkout'){
    git 'https://github.com/vsknalli/jenkins-pipeline'
  }
  stage('Compile and Package'){
    sh 'mvn package'
  }slackSend baseUrl: 'https://hooks.slack.com/services/', 
    channel: 'devopscicd', color: 'good', 
    message: 'slack notification test', 
    teamDomain: 'devopscicd', 
    tokenCredentialId: 'slack-demo'
  stage(Slack Notification){
    
    
  }
}
