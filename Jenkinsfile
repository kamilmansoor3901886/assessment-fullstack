pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                    // Try to detect branch name safely
                    def branch = sh(script: "git rev-parse --abbrev-ref HEAD || git symbolic-ref --short HEAD", returnStdout: true).trim()
                    
                    // As fallback, check environment (useful if job was triggered from webhook/PR)
                    if (branch == "HEAD" || branch == "") {
                        branch = env.GIT_BRANCH ?: env.BRANCH_NAME ?: "unknown"
                    }

                    echo "Hello World - Branch name: ${branch}"
                }
            }
        }
    }
}
