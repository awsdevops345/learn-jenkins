pipeline {
    agent {
    node {
        label 'AGENT-1'
        
    }
}
    environment { 
        GREETING = 'Good Morning'
    }

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
                sh """
                echo "shell script"
                env
                """
            }
        }
    }

     post { 
        always { 
            echo 'I will always say Hello again!'
        }

        failure {
            echo 'this runs when pipeline failed'
        }
        success {
            echo 'this runs when pipeline success'
        }
    }
}