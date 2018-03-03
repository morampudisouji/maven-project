pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                build job: 'maven-project'
                build job: 'firstjob'
            }
        }
        stage ('Deploy to Staging'){
            steps {
                build job: 'Deploy-to-staging1'
            }
          }

        stage ('checkstyle checking'){
             steps {
                build job: 'checkstyleMavenProject'  
             } 
        }
    }       
}
