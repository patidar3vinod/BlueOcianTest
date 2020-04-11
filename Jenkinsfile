pipeline {
  agent any
  stages {
    stage('Code') {
      steps {
        bat 'echo \'Code Step\''
      }
    }

    stage('Git') {
      steps {
        git(url: 'https://github.com/patidar3vinod/BlueOcianTest.git', branch: 'master', changelog: true, poll: true)
      }
    }

    stage('Build') {
      steps {
        bat 'mvn clean test'
      }
    }

    stage('deploy') {
      steps {
        bat 'echo \'deployed\''
      }
    }

  }
}