pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Python Pipeline') {
            steps {
                sh '''
                echo "Running Python pipeline"
                python3 app.py
                '''
            }
        }

        stage('.NET Restore') {
            steps {
                sh '''
                cd JenkinsDotNetDemo
                dotnet restore
                '''
            }
        }

        stage('.NET Build') {
            steps {
                sh '''
                cd JenkinsDotNetDemo
                dotnet build --configuration Release
                '''
            }
        }

        stage('.NET Run') {
            steps {
                sh '''
                cd JenkinsDotNetDemo
                dotnet run
                '''
            }
        }
    }
}
