pipeline {
    agent{ 
        node {
        label 'Agent-1'
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
    post{
        always{
            echo 'I will always say Hello again!'
        }
    }
}