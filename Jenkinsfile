pipeline {
    agent { 
        node { 
            label 'py-agent'
            }
      }
    triggers {

        pollSCM('H/5 * * * *')

    }

    stages {
        stage('Requirements') {
            steps {
                echo "Installing Requirements.."
                sh '''
                cd myapp
                pip install -r requirements.txt 
                '''
            }



        }

        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                python3 myapp/hello.py
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing test stuff.."
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}