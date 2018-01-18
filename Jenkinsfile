pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'mvn clean package'
            }
            post{
                success{
                    echo 'now archiving'
                    archiveArtifacts artifacts:'**/target/*.war'
                }
            }
            stage('deloy to stage'){
                steps{
                    build job: 'deploy-to-stage'
                }
            }

        }
    }
}
