pipeline {
  agent any
  environment {
    PATH ="/opt/maven3/bin:$PATH"
  }
  stages {
    stage('Build') {
      steps
      {
       sh "mvn clean package"
      }
    }
  }
}
