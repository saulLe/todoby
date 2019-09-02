pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
    }

  }
  stages {
    stage('ls') {
      steps {
        sh '''
ls'''
      }
    }
    stage('cd') {
      steps {
        sh 'cd eureka'
      }
    }
    stage('mvn') {
      steps {
        sh 'ls'
      }
    }
    stage('m') {
      steps {
        sh 'mvn -B -DskipTests clean package'
      }
    }
  }
}