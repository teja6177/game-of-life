node('node1') {
	stage('SourceCode') {
		git branch: 'sprint_devlop', url: 'https://github.com/teja6177/game-of-life.git'
	}
	
	stage('Build The Code') {
		sh 'mvn clean package'
	}
	
	stage('Archiving The Artifacts & Junit Test Results') {
		junit '**/surefire-reports/*.xml'
                archiveArtifacts artifacts: '**/*.war', followSymlinks: false
	}
}
