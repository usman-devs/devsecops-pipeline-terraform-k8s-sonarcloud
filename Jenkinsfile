pipeline {
  agent any
  tools { 
        maven 'Maven_3_0_5'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=usmanbuggywebapp -Dsonar.organization=usmanbuggywebapp -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=d96ed3fed3dea752cee4ec0a7316d23d704d1b8d'
			}
        } 
  }
}
