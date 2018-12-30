pipeline {
    agent any
    tools{
        maven 'DefaultMaven'
    }
    stages {
        stage('Build'){
            steps{
                sh 'mvn clean package'
            }
            post{
                success{
                    echo 'now Archiving..'
                    archiveArtifacts artifacts:'**/target/*.war'
                }
            }
        }
        stage('Deploy'){
            steps{
                echo "Testing.."
            }
        }
    }
}