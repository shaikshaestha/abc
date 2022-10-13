pipeline {
    agent any 
    stages {
        stage ('hello') {
            steps {
                sh '''
                rm -rf *
                git clone https://github.com/shaikshaestha/abc.git
                '''
            }
        }
        stage ('maven_clean') {
            
            steps {
                sh '''
                cd abc
                mvn clean
                '''
            }
        }
        
        stage ('maven_compile') {
            steps {
                sh '''
                cd abc
                mvn compile
                '''
            }
        }
        
       
        stage ('maven_test') {
            steps {
                sh '''
                cd abc
                mvn test install package
                '''
            }
        }
    }
}
