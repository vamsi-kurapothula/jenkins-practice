pipeline {
   agent {
        node {
            label 'AGENT-1'
        }
    }
    environment {
        COURSE = 'jenkins'
    }
    options {
        timeout(time: 30, unit: 'MINUTES') 
        disableConcurrentBuilds()
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Hello bulid"
                        env

                    """
                }
                
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Testing..'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying....'
                }
                
            }
        }
    }
      post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success {
            echo 'hi this is success'
            deleteDir()
        }
        failure {
            echo 'hi, this is failure'
        }
    }
}