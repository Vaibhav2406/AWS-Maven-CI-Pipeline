pipeline {
    agent any
    environment {
    MAVEN_HOME = tool name: 'Maven3.6', type: 'maven'
}
    stages {
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/Vaibhav2406/AWS-Maven-CI-Pipeline.git'
            }
        }    
        stage('Maven Compile') {
            steps {
               sh "mvn compile"
            }
        }
        stage('Maven CodeReview') {
            steps {
               sh "mvn -P metrics pmd:pmd"
            }
        }
        stage('Maven Unit Testing') {
            steps {
               sh "mvn test"
            }
        }
        stage('Maven Code Coverage') {
            steps {
               sh "mvn cobertura:cobertura -Dcobertura.report.format=xml"
            }
        }
    }

}
