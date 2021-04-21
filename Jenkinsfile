pipeline {
  agent none
  stages {
    stage("build & SonarQube analysis") {
      agent any
      steps {
        withSonarQubeEnv('sonarqube') {
           sh '''/Users/Nasir.Abbas/Downloads/sonar-scanner-4.6.0.2311-macosx/bin/sonar-scanner \
           -Dsonar.projectKey=PythonJenkins'''
        }
      }
    }
  }
}
