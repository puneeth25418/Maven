pipeline {
    agent any  // Use any available agent

    tools {
jdk 'jdk'
maven 'maven'
        gradle 'gradle'  // Ensure this matches the name configured in Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/puneeth25418/My-Maven-App'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'  // Run Maven build
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'  // Run unit tests
            }
        }
}

        
        
       
        stage('Run Application') {
            steps {
                // Start the JAR application
                sh 'java -jar target/MyMavenApp-1.0-SNAPSHOT.jar'
            }
        }

        
    }
