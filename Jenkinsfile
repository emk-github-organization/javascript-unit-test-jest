node ("docker-agent-python") {
  stage('SCM') {
    git branch: 'main', url: ' https://github.com/emk-github-organization/javascript-unit-test-jest.git'
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'sonar-scanner';
    withSonarQubeEnv('sonarqube') {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
