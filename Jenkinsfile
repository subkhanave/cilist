pipeline {
    agent {label 'jenkins-worker'}
    
    environment {
        GIT_COMMIT_SHORT = sh(returnStdout: true, script: '''echo $GIT_COMMIT | head -c 7''')
    }

    stages {
        stage('Prepare .env') {
            steps {
                sh 'echo GIT_COMMIT_SHORT=$(echo $GIT_COMMIT_SHORT) > .env'
            }
        }
        stage('hello-world') {
            steps {
                sh 'echo "hello-world"'
            }
        }

    }
}
