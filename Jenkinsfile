node {
  stage('SCM Chekcout'){
    git 'https://github.com/vsknalli/jenkins-pipeline'    
  }
  stage('Compile & packae'){
    sh "mvn clean package"
    
  }
   
}


