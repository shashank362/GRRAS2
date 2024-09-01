pipeline {
    agent {
     label 'slave-label'       
    }
    stages {
        stage('Checkout') {
             steps{
                 git 'https://github.com/shashank362/GRRAS2.git'
            }
        }
    stage('Build'){
             steps{
                 sh JAVA_HOME=/home/shanks/slavedir/jdk-11.0.24 /home/shanks/slavedir/apache-maven-3.9.9/bin/mvn install'
            }
       }
    stage('Deploy'){
            steps{
                 sh 'cp target/GRRAS2.war /home/shanks/slavedir/apache-tomcat-9.0.93/webapps'
           }
       }
   }
}
