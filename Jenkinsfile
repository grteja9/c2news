pipeline{
    agent any
    stages{
        stage('sonar quality check'){
            agent{
                docker{
                  sudo  image 'maven'
                }
            }
            steps{
                script {
               withSonarQubeEnv(credentialsId: 'sonar-token') {
            sh 'mvn clean package sonar:sonar'
}
                }
            }

        }
    }
}
