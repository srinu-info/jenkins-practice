pipeline {
    agent {
        label 'AGENT-1'
    }
    environment{
        name='jenkins'

    }

    stages {
        stage('Build') {
            steps {
                script{
                     sh """
                     echo '****************
                     env
                     """
                }               
            }
        }
        stage('Test') {
            steps {
               script{
                     echo 'Teesting..'
                }               
            }
            }        
        stage('Deploy') {
            steps {
               script{
                     echo 'Deploying..'
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