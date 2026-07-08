pipeline {
    agent {
        label 'AGENT-1'
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
            }
        }
    }
    post{
        always{
            echo 'i will always run'
        }
        success{
            echo 'i will run when success'
        }
        failure{
            echo 'i will run on failure'
        }
    }
}