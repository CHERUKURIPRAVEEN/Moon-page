pipeline {
    agent any
    
    tools{
        jdk 'jdk11'
        maven 'maven3'
    }

    stages {
        stage('git checkout') {
            steps {
                git 'https://github.com/veerababu5/MOONPAGE-PROJECT.git'
            }
        }
        
        stage('maven build') {
            steps {
                sh "mvn clean package"
            }
        }
        
        stage("Deploy To Tomcat"){
            steps{
                sh "sudo cp -r /var/lib/jenkins/workspace/Samplepipeline/target/MoonPageWebApp.war /opt/tomcat/webapps/ "
            }
        }
        
    }
}
