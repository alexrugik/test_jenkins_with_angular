pipeline {
    agent any
    stages {
        stage('Lint') {
            steps {
                bat 'node -v';
                bat 'npm -v';
                bat 'npm run lint';
            }
        }
       stage('Test') {
            steps {
                bat 'node -v';
                bat 'npm -v';
                bat 'npm run test';
            }
        }
        stage('Build') {
            steps {
                bat 'node -v';
                bat 'npm -v';
                bat 'npm run build';
            }
        }
    }

    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
