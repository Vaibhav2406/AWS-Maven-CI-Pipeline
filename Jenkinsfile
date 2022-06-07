pipeline {
    agent any
    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven3.6"
    }
    stages {    
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
        stage('Maven Package') {
            steps {
               sh "mvn package"
            }
        }
    }

}
