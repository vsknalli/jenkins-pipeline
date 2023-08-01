node{
  stage('SCM checkout'){
    git 'https://github.com/vsknalli/jenkins-pipeline.git'
  }
  stage('Compile and package'){
    sh 'mvn package'
  }
}
