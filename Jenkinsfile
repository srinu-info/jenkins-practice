pipeline {
    agent {
        label 'AGENT-1'
    }
    environment{
        name='jenkins'

    }
    options{
        timeout(time: 30, unit: 'SECONDS')
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage('Build') {
            steps {
                script{
                     sh """
                     echo '*****************'
                     sleep 10
                     env
                     echo "hello- ${params.PERSON}"
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