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
           echo 'Now Archiving...testing'
           archiveArtifacts artifacts :'**/*.war'
           }
       }
    }
	stage('Deploy'){
	  steps{
	  build job:'deploy to staging'
       } 
     }
   }
}
