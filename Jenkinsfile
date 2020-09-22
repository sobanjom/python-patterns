pipeline {
  agent none
  stages {
    stage("build & SonarQube analysis") {
      agent any
      steps {
        withSonarQubeEnv('sonarqube') {
           sh "/Users/Michael.Sobanjo/Downloads/sonar-scanner-4.4.0.2170-macosx/bin/sonar-scanner" 
        }
      }
    }
  }
}
