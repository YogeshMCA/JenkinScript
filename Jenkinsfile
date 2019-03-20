pipeline {
    agent {
        node {
            label 'master'
        }
    }
    stages {
        stage('Clone') {
            steps {
                git branch : 'master',
                    credentialsId:'994dba1c-cabc-4d5f-b9d3-8c72366daefb'
                    url: 'https://github.com/YogeshMCA/Spring-Boot-DEV.git'
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
