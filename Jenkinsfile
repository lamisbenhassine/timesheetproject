pipeline {
    agent any

    tools {
        jdk 'JAVA_HOME'
        maven 'M2_HOME'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/hwafa/timesheetproject.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'java -version'
                sh 'mvn -version'
                sh 'mvn clean compile'
            }
        }
    }
}
