pipeline{
    agent any
    tools{
        maven 'Maven_home'
    }
    stages{
        stage("SCM Checkout"){
            steps{
            git 'https://github.com/mekalajayaraj/simple-java-maven-app.git'
            }
        }
        stage("Maven Build"){
            steps{
                bat 'mvn clean package'
            }
        }
         stage('Test') {
            steps {
                bat 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        stage('Deploy') {
            steps {
                bat 'make publish'
            }
        }
        
    }
}
