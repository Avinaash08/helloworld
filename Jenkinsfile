pipeline {
  agent any
  stages {
    stage('Git Checkout') {
      steps
      {
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'git', url: 'https://github.com/Avinaash08/helloworld.git']]])      
      }
    }
  }
}
