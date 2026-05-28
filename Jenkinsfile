pipeline {
    agent{ 
        node {
        label 'Agent-1'
       }  
    }
    environment{
        COURSE = "Jenkins"
    }
    options{
        timeout(time: 1, unit: 'SECONDS')
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                    echo "Build"
                    echo $COURSE
                    sleep 10
                    env
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh """
                    echo "Test"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh """
                    echo "Deploy"
                    """
                }
            }
        }
    }
    post{
        always{
            echo 'I will always say Hello again!'
            cleanWs()
        }
        success{
            echo 'I will say Hello again only if the build is successful!'
        }
        failure{
            echo 'I will say Hello again only if the build fails!'
        }
        aborted{
            echo 'I will say Hello again only if the build is aborted!'
        }
    }
}