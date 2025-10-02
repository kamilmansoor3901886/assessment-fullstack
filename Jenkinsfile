pipeline {
    agent any   // Runs on any available agent

    stages {
        stage('Hello') {
            steps {
                script {
                    echo "Hello World - Branch name: ${env.BRANCH_NAME}"
                }
            }
        }
    }
}