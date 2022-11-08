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
       sh "mv target/*.war target/myweb.war" 
      }
    }
    stage('Deploy') {
      steps {
        sh '''
        cp target/myweb.war /opt/tomcat/webapps
        '''
      }
    }
  }
}
