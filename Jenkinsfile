node ('JDK8'){
    stage ('SourceCode') {
        // get the code from git repo on the branch sprint1_devlope
        git branch: 'sprint1_devlope', url: 'https://github.com/Sandip090/game-of-life.git'
    }
    stage ('Build the code') {
        sh 'mvn clean package'
    }
    stage ('Archiving and Test Result'){
        junit '//**surefire-reports/*.xml'
        archiveArtifacts artifacts: '**/*.war', followSymlinks: false
}
}
