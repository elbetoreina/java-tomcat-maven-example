pipeline {
    agent any
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                echo "PATH = ${PATH}"
                echo "M2_HOME = ${env.M2_HOME}"
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
