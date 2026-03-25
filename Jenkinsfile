pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/rahulguthi033-tech/devops-project-1.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                sh 'mvn package -DskipTests'
                sh 'cp target/mavenproject.war /opt/tomcat/webapps/'
            }
        }
    }
}
