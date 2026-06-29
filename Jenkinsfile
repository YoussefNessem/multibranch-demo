pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Building ${env.BRANCH_NAME}"
            }
        }
        stage('Test') {
            steps {
                when{
                  anyOf{
                      branch'main'
                      branch'dev'
                  }
                }
                steps {
                    echo "Running Test ${env.BRANCH_NAME}"
                }
            }
        }
        stage('Deploy') {
            when{
                branch'main'
                }
            }
            steps {
                echo "Deploying..."
            }
        }
    }
