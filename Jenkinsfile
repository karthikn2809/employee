pipeline {
    agent any
 
    stages {
        stage('Clean') {
            steps {
            	echo "clean"
                bat 'mvn clean'
            }
        }
        
        stage('Install') {
            steps {
                echo "install"
                bat 'mvn install'
            }
        }
        
        stage('Test') {
            steps {
             echo "test"
             bat 'mvn test'
            }
        }
        
        stage('Verify') {
            steps {
             echo "verify"
             bat 'mvn verify'
            }
        }
 
        stage('Deploy') {
            steps {
                echo 'application deployed.'
            }
        }
    }
 
    post {
        failure {
            echo 'FAILED'
        }
    }
}
 
