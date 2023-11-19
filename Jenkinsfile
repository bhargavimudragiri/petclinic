pipeline {
    agent any 
    
    tools{
        jdk 'jdk11'
        maven 'maven3'
    }
    stages{
        
        stage("Git Checkout"){
            steps{
                git branch: 'future1', changelog: false, poll: false, url: 'https://github.com/jaiswaladi246/Petclinic.git'
            }
        }
        
        stage("Compile"){
            steps{
                sh "mvn clean compile"
            }
        }
         stage("Build"){
            steps{
                sh " mvn clean install"
            }
        }
        
    }
}
