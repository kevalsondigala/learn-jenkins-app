pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sh 'echo "Hello Developer"'
            }
        }
        stage('Check os version') {
            staps {
                echo 'Checking in progress...'
                echo 'Have some patience'
                echo 'go drink some water'
                sh 'cat /etc/os-release'
            }
        }
    }
}
