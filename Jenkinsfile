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
                bat 'cd ${C:\\Users\\Admin\\.jenkins\\workspace\\Test01}'
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
