pipeline {
    agent any

    tools {
        maven 'Maven
    }

    stages {

        stage('Checkout') {
            steps {
git url: 'https://github.com/omkar183/MyMavenSeleniumApp.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed'
        }
        success {
            echo 'Build SUCCESS '
        }
        failure {
            echo 'Build FAILED '
        }
    }
}
