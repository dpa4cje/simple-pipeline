pipeline {
  agent {
    kubernetes {
      label 'kubernetes'
      containerTemplate {
        name 'maven'
        image 'maven:3.3.9-jdk-8-alpine'
        ttyEnabled true
        command 'cat'
      }
    }
  }
  stages {
    stage('Maven in k8s') {
        steps {
            container('maven') {
                sh 'mvn -version'
            }
        }
    }
}
