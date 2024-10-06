pipeline {
  agent {
    label {
      label 'Node-1'
      retries 3
    }
  }

  triggers {
    githubPush()
  }

  stages {
    stage ('Build') {
      steps {
        echo 'Running build automation'
        sh '''
          chmod +x ./gradlew
          ./gradlew build
        '''
        archiveArtifacts artifacts: 'app/dist/app.zip'
      }
    }
  }
} 
