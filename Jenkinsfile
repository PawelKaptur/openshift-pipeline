node('maven') {
  stage('Clean') {
    git url: "https://github.com/PawelKaptur/openshift-pipeline.git"
    sh "mvn clean"
  }
  
  stage('Build') {
    sh "mvn package"
  }
  
  stage('Test') {
    sh "mvn test"
  }
}