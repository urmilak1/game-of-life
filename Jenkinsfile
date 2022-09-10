pipeline {
    agent any
       
     tools { 
        maven 'apache-maven-3.8.6' 
        jdk 'jdk11' 
    }
    
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
       stage("build") {
            agent any
            steps {
              
                sh 'mvn clean package '
              }
            }
        }    
    }

