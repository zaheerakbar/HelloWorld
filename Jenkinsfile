pipeline {
  stages {
    stage('Maven Install') {
      agent {
        docker {
          image 'maven:3.5.0'
        }
      }
      steps {
        bat 'mvn clean install'
      }
    } 
  }
}
