pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('buildQ') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
