pipeline {
    agent {
        node {
            label 'master'
        }
    }
    parameters{
        String(name:'PROJ_PATH',defaultValue:'C:\\Users\\Admin\\.jenkins\\workspace\\Test01',description:'Project Path')
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
                bat "cd ${params.PROJ_PATH}"
                mvn package                
            }
        }
    }
    stages {
        stage('Deploy') {
            steps {
                bat "cd ${params.PROJ_PATH}/target"
                bat "java -jar spring-boot-web-app-0.0.1-SNAPSHOT.war"
                
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
