pipeline {
    agent any
    stages {
        stage ('Initialize') {
            steps {

                echo ${PATH}
                sh '''
                echo "PATH = ${PATH}"
                echo "M2_HOME = ${M2_HOME}"                
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
