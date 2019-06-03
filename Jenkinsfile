pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean -Dhttp.proxyHost=web-proxy.sgp.hp.com -Dhttp.proxyPort=8080'
      }
    }
  }
}
