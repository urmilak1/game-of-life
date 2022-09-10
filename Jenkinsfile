pipeline {
    agent any
       tools {
        maven 'MAVEN_HOME' 
    }
     stages {
       stage('Load Tools') {
              steps {
                 sh "mvn -version"
              }
         }
    }
   
  }

