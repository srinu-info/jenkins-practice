pipeline {
    agent {
        label 'AGENT-1'
    }
    environment{
        name='jenkins'

    }
    options{
        timeout:{time: 10, unit: 'SECONDS'}
        disableConsurrentBuilds()
    }

    stages {
        stage('Build') {
            steps {
                script{
                     sh """
                     echo '****************'
                     sleep 10
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