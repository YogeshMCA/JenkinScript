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
    }
    stages {
        stage('Build') {
            steps {
                mvn package                
            }
        }
    }
    stages {
        stage('Deploy') {
            steps {
                java -jar spring-boot-web-app-0.0.1-SNAPSHOT.war
                
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
