pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out code'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip3 install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest'
            }
        }

    }

    post {
        success {
            echo 'Pipeline Successful'
        }

        failure {
            echo 'Pipeline Failed'
        }
    }

}
