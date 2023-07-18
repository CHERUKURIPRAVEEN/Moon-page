pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                git credentialsId: 'Jenkins-Github-Admin', url: 'https://github.com/CHERUKURIPRAVEEN/MOONPAGE-PROJECT.git'
            }
        }
        stage('BranchValidation') {
            steps{
                echo "pipeling running in ${branch}"
            }
        }
        stage('mvn-build') {
            steps {
                echo "creating archive using maven"
            }
        }
        stage('sonar-scanner') {
            steps {
                echo "static code analysis using sonar"
            }
        }
        stage('upload') {
            steps {
                script {
                    echo "upload artifacts using nexus"
                }
            }
        }
        stage('deploy'){
            steps{
                script{
                    echo "deploy archive using ansible"
                }
            }
        }
    }
}
