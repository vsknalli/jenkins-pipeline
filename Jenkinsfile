node{
  stage('SCM checkout'){
    git 'https://github.com/vsknalli/jenkins-pipeline'
  }
  stage('Compile and package'){
    sh 'mvn install'
  }
}
