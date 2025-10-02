pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                ls -la
                node --version
                npm --version
                node ci
                npm run build
                ls -la
                '''
            }
        }
    }
}
