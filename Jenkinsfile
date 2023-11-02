pipeline {
    agent { 
        node {
            label 'docker-agent-python'
            }
      }
    triggers {
        pollSCM '*/ * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building stage.."
                sh '''
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing stage.."
                sh '''
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver stage....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
