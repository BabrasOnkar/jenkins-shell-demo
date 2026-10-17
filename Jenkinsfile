
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Downloading code from GitHub...'
                checkout scm
            }
        }

        stage('Run Shell Script') {
            steps {
                echo 'Executing script.sh...'
                sh 'bash script.sh'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed. Check the console logs.'
        }
    }
}
