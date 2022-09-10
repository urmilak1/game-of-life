pipeline {
    agent any
    
       options {
        timeout(time: 50, unit: 'MINUTES') 
    }
     triggers {
        cron('25 18 * * *')
    }

    stages {

        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
       stage("build & SonarQube analysis") {
            agent any
            steps {
              withSonarQubeEnv('sonarqube-8.9.9.56886') {
                sh 'mvn clean package sonar:sonar'
              }
            }
          }
    
    }
}
