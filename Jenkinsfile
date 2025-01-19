pipeline {
    agent any
    tools {
        jdk 'JDK11'
        maven 'Maven3'
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Mohsenghafoorydotin/java-hello-world-with-maven.git'
            }
        }
        stage('build') {
            steps{
                sh 'mvn clean compile'
            }
        }
        stage('Test') {
            steps{
                sh 'mvn test'
            }
        }
    }
    post {
        always {
            junit '**/target/surefire-reports/*.xml'
        }
    }
}
