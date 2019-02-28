node('maven') {
  stage('Clean') {
    git url: "https://github.com/PawelKaptur/openshift-pipeline.git"
    sh "mvn clean"
  }
  
  stage('Compile') {
    sh "mvn compile"
     }
  
  stage('Install') {
    sh "mvn install"
  }
  
  stage('Build') {
    sh "mvn package"
  }
  
  stage('Test') {
    parallel(
      "Cart Tests": {
        sh "mvn verify -P cart-tests"
      },
      "Discount Tests": {
        sh "mvn verify -P discount-tests"
      }
    )
  }
  }