pipeline {
    agent any
       tools {
        maven 'MAVEN_HOME' 
        jdk 'jdk'
    }
     stages {
       stage('Load Tools') {
              steps {
                 sh "mvn -version"
                 sh "jdk -version"
              }
         }
    }
   
  }
