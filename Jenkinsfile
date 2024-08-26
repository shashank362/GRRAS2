pipeline {
    agent any

    stages {
        stage('Checkout') {
             steps{
                 git 'https://github.com/shashank362/GRRAS2.git'
            }
        }
    stage('Build'){
             steps{
                 sh 'mvn install' 
            }
       }
    stage('Deploy'){
            steps{
                 sh 'cp target/GRRAS2.war /home/shashank/extracted/apache-tomcat-9.0.93/webapps'
           }
       }
   }
}
