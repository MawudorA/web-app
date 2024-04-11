pipeline {
    agent any
    tools {
        maven "maven3.9.6"
    }
    stages{
        stage ('git clone repository') {
            steps { 
                git branch: 'main', url: 'https://github.com/MawudorA/web-app.git'
            }
        }
        stage ('build with maven') {
            steps {
                sh "mvn clean"
            }
        }

         stage ('testing with maven') {
            steps {
                sh "mvn test" 
            }
        }
        stage (' packaging with maven') {
            steps {
                sh "mvn package"
            }
        }
    }
}