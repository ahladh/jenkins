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
                echo "Current Workspace ${workspace}"
            }
        }
        stage('Sanity Check'){
        input 'Shall I complete the job?'
        }

    }
    post {
        always{
         echo "I am cleaning the workspace"
        //deleteDir()
        }
    }
}
