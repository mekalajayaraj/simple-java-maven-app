pipeline{
    agent any
    tools{
        maven 'maven'
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
    }
}
