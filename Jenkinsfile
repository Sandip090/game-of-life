pipeline {
agent { label 'JDK8' }
triggers { pollSCM('* * * * *') }
stages {
       stage ('source code') {
       steps {
             git branch: 'sprint1_devlope', url: 'https://github.com/Sandip090/game-of-life.git'
	     }
          }
      stage ('Build') {
      steps {
            sh 'mvn clean package'
	    }
	 }

     stage ('Archive and Test results') {
     steps {
           junit '**/surefire-reports/*.xml'
	   archiveArtifacts artifacts: '**/*.war', followSymlinks: false
	   }
	   }
	   }
	   }
     
