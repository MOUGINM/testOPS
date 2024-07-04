pipeline {
    agent any

    stages {
        stage('Setup') {
            steps {
                echo 'Setting up the environment...'
                sh 'python3 --version'  // Affiche la version de Python
            }
        }
        stage('Print Message') {
            steps {
                echo 'Printing a simple message...'
                sh 'python3 -c "print(\'Hello, Jenkins!\')"'
            }
        }
        stage('Run Simple Test') {
            steps {
                echo 'Running a simple test...'
                sh 'python3 -c "assert 1 == 1"'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed!'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
