pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Building ${env.BRANCH_NAME}"
            }
        }
        stage('Run Script') {
            steps {
                sh 'bash script.sh'
            }
        }
    }
}
