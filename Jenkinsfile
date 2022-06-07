pipeline {
    agent any
    {
       tool name: 'Maven3.6', type: 'maven'
    }
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
