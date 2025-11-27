pipeline {
    agent any

    tools {
        // ⚠️ Les noms DOIVENT être exactement
        // ceux définis dans "Global Tool Configuration"
        jdk 'JDK-17'
        maven 'Maven-3.9.6'
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
