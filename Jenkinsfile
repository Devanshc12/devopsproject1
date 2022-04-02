pipeline{
    agent any
    environment {
       PATH = ";c:\\Windows\\System32"
   }
    tools { 
        maven 'MAVEN_HOME'
        jdk 'JAVA_HOME' 
    }
    stages{
       
       stage('Git clone'){
            steps{
                git branch: 'main', changelog: false, credentialsId: 'f9dcdd6d-8985-49ef-b10a-c17a8e9fdb8b', poll: false, url: 'https://github.com/Devanshc12/devopsproject1.git'
            }
        }        
    
    
        stage('Build'){
            steps{
             bat 'mvn clean install'
            }
        }
    }
}
