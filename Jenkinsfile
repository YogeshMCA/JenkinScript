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
                    url: 'https://github.com/YogeshMCA/Spring-Boot-DEV.git',
                    credentialsId:'994dba1c-cabc-4d5f-b9d3-8c72366daefb',
                    branch : 'master'                    
                )
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
 }
}
