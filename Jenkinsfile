node('maven') {
  stage('Clean install') {
    git url: "https://github.com/PawelKaptur/openshift-pipeline.git"
    sh "mvn clean install"
  }
  
  stage('Build') {
    sh "mvn package"
  }
  
  stage('Test') {
    sh "mvn test"
  }
  }