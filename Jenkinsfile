pipeline {
    agent any
    stages {
        stage ('Build Servlet Project') {
            steps {
                sh 'mvn clean package'
            }
            post{
                echo 'Now archiving...'
                archiveArtifacts artifacts : '**/*.war'
            }
        }
    }
}
