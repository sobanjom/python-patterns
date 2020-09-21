node {
  stage('SCM') {
    git 'https://github.com/sobanjom/python-patterns.git'
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'SonarScanner 4.0';
    withSonarQubeEnv('SonarQube') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
