pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }

    //build
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    // post build
    post { 
        always { 
            echo 'I will always say Hello again!'
        }

        failure { 
            echo 'this runs when pipeline is failed, used genereally to send some alerts'
        }

        success { 
            echo 'I will say hello when pipeline is success'
        }
    }
}