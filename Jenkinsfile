pipeline {
    agent any

    stages {
        stage('Hello World') {
            steps {
                script {
                    echo "Hello from Jenkins!"
                    echo "Current branch: ${env.BRANCH_NAME}"
                }
            }
        }
    }
}
