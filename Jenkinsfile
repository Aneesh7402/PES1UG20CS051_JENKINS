pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello hello.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './hello'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deployment successful(PES1UG20CS051)'
            }
        }
    }

    post {
        always {
            script {
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed(PES1UG20CS051)'
                }
            }
        }
    }
}
