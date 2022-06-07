pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/Vaibhav2406/AWS-Maven-CI-Pipeline.git'
            }
        }    
        stage('Maven Commit') {
            steps {
               maven 'commit'
            }
        }
        
    }

}
