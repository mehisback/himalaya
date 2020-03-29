pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo "I\'m trying to build"'
        sh 'echo "build step is complete"'
      }
    }

    stage('Testing') {
      parallel {
        stage('Testing') {
          steps {
            sh 'echo "Testing has begun"'
          }
        }

        stage('Testing P1') {
          agent any
          steps {
            sh 'echo "testing 123"'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sh 'echo "rsync the build to prod servers"'
      }
    }

  }
}