pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh 'mvn --version'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testando o projeto determinantemente"'
            }
        }
    }
    post {
        always {
            junit 'build/reports/**/*.xml'
        }
    }
}