pipeline {
    agent {
        docker {
            image 'node:18-alpine'
            reuseNode true
        }
    }

    stages {
        stage('Build') {
            steps {
                sh '''
                    node --version
                    npm --version
                    npm ci
                    npm run build
                '''
            }
        }

        stage('Test') {
            steps {
                sh 'ls -la'
                sh 'test -f build/index.html'
                sh 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                    npm install -g netlify-cli
                    netlify --version
                '''
            }
        }
    }
}
