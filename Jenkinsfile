node {
  stage('SCM Chekcout'){
    git 'https://github.com/vsknalli/jenkins-pipeline'    
  }
  stage('Compile & packae'){
    // get maven hoem path
    def mavenhome = tool name: 'maven-3', type: 'maven'
    sh "${mavenhome}/bin/mvn package"
  }
  
}


