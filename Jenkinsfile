pipeline {
    agent { node { label 'osboxes' } }
    stages {
        stage('Example clean') {
            steps {
                sh "rm -rf my-app"
                sh "git clone https://github.com/connectme2soft/my-app.git"
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
        stage(Maven package') {
            steps {
                sh "mvn package -f my-app"
            }
        }
    }
}
