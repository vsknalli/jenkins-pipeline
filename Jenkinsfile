node {
  stage('SCM Chekcout'){
    git 'https://github.com/vsknalli/jenkins-pipeline'    
  }
  stage('Compile & packae'){
    // get maven hoem path
    def mavenhome = tool name: 'maven-3.9.3', type: 'maven'
    sh "${mavenhome}/bin/mvn package"
  }
  stage('SonarQube Analysis'){
    def mvnHome =  tool name: 'maven-3.9.3', type: 'maven'
    withSonarQubeEnv('sonar-6'){
      sh "${mvnHome}/bin/mvn sonar:sonar"
    }
  }
          
  stage('Slack Notifications'){
    slackSend baseUrl: 'https://hooks.slack.com/services/', 
      channel: '#devopscicd', 
      color: 'good', 
      message: 'Welcome to SenthilVeeranans\'s DevOps World...!!!', 
      tokenCredentialId: 'slack'
  }
  
}


