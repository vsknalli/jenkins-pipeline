node{
  stage('SCM Checkout'){
    git 'https://github.com/vsknalli/jenkins-pipeline'
  }
  stage('Compile and Package'){
    sh 'mvn package'
  }
}
