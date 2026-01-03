pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code checked out from Git'
                sh 'ls -l'
            }
        }

        stage('Hello') {
            steps {
                sh 'echo "Hello Shivam, Pipeline is running from Jenkinsfile"'
                sh 'cat hello.txt'
            }
        }
    }
}
