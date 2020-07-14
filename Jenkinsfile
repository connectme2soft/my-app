pipeline {
    agent { node { label 'osboxes' } }
    stages {
        stage('Mavene clean') {
            steps {
            
                
                sh "mvn clean -f my-app"
            }
        }
        
        stage('Maven install') {
            
            steps {
                sh "mvn install -f my-app"
            }
        }
        stage('Maven test') {
            steps {
                sh "mvn test -f my-app"
            }
        }
        stage('Maven package') {
            steps {
                sh "mvn package -f my-app"
            }
        }
    }
}
