pipeline {
agent any
tools {
  maven 'localMaven'
}
stages{
  stage('Build'){
  steps { 
       sh 'mvn clean package'
      }
post {
  success { 
           echo 'Now Archiving...test'
           archiveArtifacts artifacts :'**/target/*.war'
           }
       }
    }
  }
}
