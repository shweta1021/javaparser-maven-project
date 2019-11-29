pipeline {
   agent any

   stages {
       stage('SCM'){
          steps{
              git 'https://github.com/shweta1021/javaparser-maven-project.git'
          }
      }
      stage('Shell Sript') {
         steps {
            sh label: '', script: 'mvn install'
         }
      }
      
      stage('Build'){
          steps{
             build 'sonarQube_test'
          }
      }
   }
}
