pipeline {
    agent {
        label 'AGENT-1'
    }

    stages {
        stage('Build') {
            script{
            steps {
                echo 'Building..'
                }
            }
        }
        stage('Test') {
            script{
            steps {
                echo 'testing..'
                }
            }
        }
        stage('Deploy') {
            script{
            steps {
                echo 'deploying..'
                }
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