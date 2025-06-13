pipeline {
    agent any
    stages {
        stage('Clean Up') {
            steps {
                deleteDir()
            }
        }
        stage('Clone Repository') {
            steps {
                sh 'git clone https://github.com/jenkins-docs/simple-java-maven-app.git'
            }
        }
        stage('Build') {
            steps {
                dir('simple-java-maven-app') {
                    sh '/Users/akshayjadhav/Downloads/apache-maven-3.9.10/bin/mvn clean install'
                }
            }
        }
        stage('Test') {
            steps {
                dir('simple-java-maven-app') {
                    sh '/Users/akshayjadhav/Downloads/apache-maven-3.9.10/bin/mvn test'
                }
            }
        }
    }
}

