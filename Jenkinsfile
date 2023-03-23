node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'BuildSonarQube';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=minhaz044_restApi_AYcIth2YKpI6NQIQv43A"
    }
  }
}
