<<<<<<< HEAD
node('node1') {
	stage('SourceCode') {
		git branch: 'sprint_devlop', url: 'https://github.com/teja6177/game-of-life.git'
	}
	
	stage('Build The Code') {
=======
pipeline {
	agent { node1 }
	stages {
		stage('SourceCode') {
                	git branch: 'sprint_devlop', url: 'https:/github.com/teja6177/game-of-life.git' 
                }
		stage('Buid The Code') {
>>>>>>> b3b5d93 (created declarative Jenkinsfile)
		sh 'mvn clean package'
		} 
		stage('Archiving Artifact & Junit Test Results') {
 		junit '**/surefire-reports/*.xml'
                archiveArtifacts artifacts: '**/*.war', followSymlinks: false
		}
	}
}
