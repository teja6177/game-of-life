pipeline {
    agent { label 'node1' }

    stages {
        stage('SourceCode') {
            steps {
                git branch: 'sprint_devlop',
                    url: 'https://github.com/teja6177/game-of-life.git'
            }
        }

        stage('Build The Code') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Archiving Artifacts & JUnit Test Results') {
            steps {
                junit '**/surefire-reports/*.xml'
                archiveArtifacts artifacts: '**/*.war',
                    followSymlinks: false
            }
        }
    }
}
