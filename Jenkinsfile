node('master') {
    
    stage('Preparation') {
      git 'https://github.com/jglick/simple-maven-project-with-tests.git'
    }
    
    stage('Build') {
        withMaven(maven: 'M3') {
            sh 'mvn -Dmaven.test.failure.ignore clean package'
        }
    }
}
