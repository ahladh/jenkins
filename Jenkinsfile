pipeline {
    agent { docker { image 'maven:3.3.3' } }
    environment {
      Level = 'Pipeline'
    }
    stages {
        stage('buildQ') {
            environment {
            Level = 'Stage'
            }
            steps {
                echo "Level env var has higher precedence in ${Level}"
            }
        }
    }
}
