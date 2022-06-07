pipeline {
    agent any
    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven3.6"
    stages {
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/Vaibhav2406/AWS-Maven-CI-Pipeline.git'
            }
        }    
        stage('Maven Commit') {
            steps {
               mvn 'commit'
            }
        }
        
    }

}
