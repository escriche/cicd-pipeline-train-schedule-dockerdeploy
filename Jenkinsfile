pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                this.enableTimeouts(false)
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
