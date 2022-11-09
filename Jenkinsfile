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
       sh "mv target/*.jar target/myweb.jar" 
      }
    }
    stage('Deploy') {
      steps {
        sh '''
        cp target/myweb.jar /opt/tomcat/webapps
        ls /opt/tomcat/webapps/
        '''
      }
    }
  }
}
