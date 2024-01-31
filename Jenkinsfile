pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }

    environment { 
        GREETING = 'Hello Jenkins'
    }
    options {
                timeout(time: 1, unit: 'HOURS') 
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
                sh """
                    echo "Here i wrote shell script"
                    echo "$GREETING"
                    sleep 10
                """
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