node {
  stage('SCM') {
    git 'https://github.com/sobanjom/python-patterns.git'
  }
  stage('SonarQube analysis') {
    withSonarQubeEnv() { // If you have configured more than one global server connection, you can specify its name
      sh "/Users/Michael.Sobanjo/Downloads/sonar-scanner-4.4.0.2170-macosx/bin/sonar-scanner" \
                        -Dsonar.projectKey=PythonJenkins
    }
  }
}
