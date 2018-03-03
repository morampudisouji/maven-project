pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                build job: 'maven-project'
            }
        }
        stage ('Deploy to Staging'){
            steps {
                build job: 'Deploy-to-staging'
            }
          }

        stage ('checkstyle checking'){
             steps {
                build job: 'checkstyleMavenProject'  
             } 
        }
    }       
}
