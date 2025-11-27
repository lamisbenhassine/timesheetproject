pipeline {
    agent any

    tools {
        jdk 'JAVA_HOME'
        maven 'M2_HOME'
    }

    stages {

        stage('Check Java') {
            steps {
                sh 'java -version'
            }
        }

        stage('Check Maven') {
            steps {
                sh 'mvn -version'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }
    }

    post {
        success {
            echo '✅ BUILD SUCCESS'
        }
        failure {
            echo '❌ BUILD FAILED'
        }
    }
}
