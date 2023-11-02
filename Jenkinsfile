pipeline {
    agent { 
        node {
            label 'docker-agent-python'
            }
      }
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building stage.."
                sh '''
                cd myapp
                pip install -r requirements.txt
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing stage.."
                sh '''
                cd myapp
                python3 hello.py 
                python3 hello.py --name=Dinesh
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
