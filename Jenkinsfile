pipeline {
  agent none
  stages {
    stage('build') {
          agent none
          steps {
            echo "Build application-1 in windows agent"
          }
        }
    stage('scan') {
	      steps {
	      	withSonarQubeEnv(installationName: 'SQ-1'){
	      		bat "mvnw  clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.8.0.2131:sonar"
	      	}
	         echo "Run application on scan"
	      }
	    }
  }
}