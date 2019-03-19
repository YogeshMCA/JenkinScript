pipeline {
    agent {
        node {
            label 'master'
        }
    }
    stages {
        stage('Clone') {
            steps {
                git clone 'https://github.com/YogeshMCA/Spring-Boot-DEV.git'
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
