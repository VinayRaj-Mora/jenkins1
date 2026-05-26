pipeline {
    agent{ 
        node {
        label 'AGENT-01'
       }  
    }
    stages {
        stage('Build') {
            steps {
                echo "Build"
            }
        }
        stage('Test') {
            steps {
                echo "Test"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy" 
            }
        }
    }
}