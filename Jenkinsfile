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
        stage('Deploy to production'){
            steps{
                timeout(time:5,unit:'DAYS'){
                    input message: 'Approve Production Deployment'
                }

                build job: 'deploy_tomcat_production_pipeline'
            }
            post{
                success{
                    echo 'Deployment on Production is Successful'
                }
                failiure{
                    echo 'Deployment Failure on Production'
                }
            }
        }


    }
}
