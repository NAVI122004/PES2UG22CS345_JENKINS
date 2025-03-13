pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the project...'
                    sh 'make -C main'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                    sh 'cd /var/jenkins_home/workspace/PES2UG22CS330-1/main/ && ./hello_exec'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
