pipeline {
  agent {
    label {
      label 'Node-1'
      retries 2
    }
  }

  stages {
    stage ('Build') {
      steps {
        echo 'Running build automation'
        sh './gradlew build'
        archiveArtifacts artifacts: 'app/dist/app.zip'
      }
    }
  }
}  