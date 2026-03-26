pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/rahulguthi033-tech/devops-project-1.git'
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

        stage('Deploy') {
            steps {
                sh 'cp target/*.war /opt/tomcat11/webapps/'
            }
        }
    }
}
