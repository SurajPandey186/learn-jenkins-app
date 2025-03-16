pipeline {
    agent any
    stages {
        stage('Build') {
            agent {
                docker {
                    reuseNode true
                    image 'node:18-alpine'
                }
            }
            steps {
                sh '''
                  ls -la
                  npm --version
                  node --version
                  npm ci
                  npm run build
                  ls -la
                '''
            }
        }
    }
}
