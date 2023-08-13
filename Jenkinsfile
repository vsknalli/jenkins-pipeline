node{
  stage('SCM Checkout'){
    git 'https://github.com/vsknalli/jenkins-pipeline'
  }
  stage('Compile and Package'){
    sh 'mvn package'
  }
  stage('Slack Notification'){
   slackSend baseUrl: 'https://hooks.slack.com/services/', 
    channel: 'devopscicd', color: 'good', 
    message: 'slack notification test', 
    teamDomain: 'devopscicd', 
    tokenCredentialId: 'slack-demo' 
    
  }
}
