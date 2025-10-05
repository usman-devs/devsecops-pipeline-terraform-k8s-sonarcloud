pipeline {
    agent any

    tools { 
        maven 'Maven_3_0_5'  
    }

    environment {
        // Limit memory usage for Maven / Java process to prevent OOM
        MAVEN_OPTS = "-Xmx512m -Xms256m"
    }

    stages {
        stage('Compile and Run Sonar Analysis') {
            steps {	
                sh '''
                    mvn clean verify sonar:sonar \
                    -Dsonar.projectKey=usmanbuggywebapp \
                    -Dsonar.organization=usmanbuggywebapp \
                    -Dsonar.host.url=https://sonarcloud.io \
                    -Dsonar.token=d96ed3fed3dea752cee4ec0a7316d23d704d1b8d
                '''
            }
        } 
    }
}
