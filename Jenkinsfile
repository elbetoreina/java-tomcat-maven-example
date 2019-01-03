pipeline {
    agent any
    stages {
        stage ('Build Servlet Project') {
            steps {
                sh 'mvn clean package'
            }
            post{
                success{
                    echo 'Now archiving...'
                    archiveArtifacts artifacts : '**/*.war'
                }                
            }
        }
        stage('Deploy Build in Staging Area'){
            steps{
                build job : 'deploy_tomcat_staging_pipeline'
            }
        }
    }
}
