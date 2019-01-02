pipeline {
    agent any
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                echo "PATH = ${PATH}"
                echo "M2_HOME = ${MAVEN_HOME}"
                '''
            }
        }

        stage ('Build'){
            steps{
                echo 'Hello World'

            }
        }
    }
}
