pipeline {
    agent any

    stages {
        stage("build & sonarqube") {
            agent any
            steps {
              withSonarQubeEnv(credentialsId: 'Sonar_Token') {
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
    }
    
}
