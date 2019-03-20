pipeline {
    agent {
        node {
            label 'master'
        }
    }
    
    stages {
        stage('Clone') {
            steps {
                git (
                    url: 'https://github.com/YogeshMCA/Dev.git',
                    credentialsId:'d1ab25ca-428e-4845-881d-71204dd8c586',
                    branch : 'master'                    
                )
                
            }
        }
    
    stage('Build') {
            steps {
                bat 'set MAVEN_HOME=C:\\java cognizant\\apache-maven-3.5.0-bin\\apache-maven-3.5.0'
                bat 'mvn package'
                }
            }
     }
    
    post {
        success {
            echo 'Deployment Completed Successfully'
        }
        failure {
            echo 'Deployment Failed'
        }
 }
}
