pipeline {
    agent any
    options {
        ansiColor('xterm')
        }
    stages {
        stage('Maven Commit') {
            steps {
               mvn 'commit'
            }
        }
        
    }

}
