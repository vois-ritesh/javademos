pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -f javademos-master/ssgsems/pom.xml -B -DskipTests clean package'
        archiveArtifacts(artifacts: '**/target/*.war', fingerprint: true)
        sh '''mkdir /home/vois_ritesh/buildoutput/${BUILD_NUMBER}

cp **/target/*.war /home/vois_ritesh/buildoutput/${BUILD_NUMBER}'''
      }
    }

  }
}