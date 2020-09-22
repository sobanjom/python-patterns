pipeline {
  agent none
  stages {
     stage('SCM') {
    git 'https://github.com/sobanjom/python-patterns.git'
  } 
    stage("build & SonarQube analysis") {
      agent any
      steps {
        withSonarQubeEnv() {
           sh "/Users/Michael.Sobanjo/Downloads/sonar-scanner-4.4.0.2170-macosx/bin/sonar-scanner" \
           sonar.projectKey=PythonJenkins
        }
      }
    }
  }
}
