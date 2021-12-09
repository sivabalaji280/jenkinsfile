node('maven3.8.4') {
    
    stage('build'){
        
        sh '/usr/local/apache-maven-3.8.4/bin/mvn clean package'
    }
    stage('archive'){
        archiveArtifacts artifacts: '**/*.jar', followSymlinks: false
    }
    stage('Testing'){
        junit '**/TEST*.xml'
    }
}