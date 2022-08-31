pipeline {
  agent any
  stages {
    stage('compile-app') {
      steps {
        echo 'this is the compile job'
        sh 'mvn compile'
      }
    }

    stage('test-app') {
      steps {
        echo 'this is the test job'
        sh 'mvn test'
      }
    }

    stage('package-app') {
      steps {
        echo 'this is the package job'
        sh 'mvn package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'mave'
  }
  post {
    always {
      echo 'Hurray, my second pipeline is ready!'
    }

  }
}