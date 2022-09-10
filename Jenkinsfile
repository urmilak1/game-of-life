pipeline {
    agent any
       
     tools { 
        maven 'maven-3.8.6' 
        jdk 'jdk-11.0.16.1' 
    }
    
       options {
        timeout(time: 50, unit: 'MINUTES') 
    }
     triggers {
        cron('25 18 * * *')
    }

    stages {
          
        stage('Initialize'){
            steps{
                echo "JAVA_HOME = C:\Program Files\Java\jdk-11.0.16.1\bin"
                echo "M2_HOME = C:\urmila_dev\apache-maven-3.8.6-bin"
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

