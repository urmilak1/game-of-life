pipeline {
    agent {
           label 'linux-machine'
       }
       tools {
        maven 'MAVEN_HOME' 
        jdk 'jdk'
    }
     stages {
       stage('Load Tools') {
              steps {
                 echo 'i am urmila'
                  sh "mvn -version"
              }
         }
    }
   
  }
