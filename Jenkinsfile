pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                    // Get current branch name from Git
                    def branch = sh(script: "git rev-parse --abbrev-ref HEAD", returnStdout: true).trim()
                    echo "Hello World - Branch name: ${branch}"
                }
            }
        }
    }
}
