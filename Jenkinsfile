pipeline {
 agent {
 docker {
  image 'arm32v7/maven:3.6-jdk-12-alpine' args '-v /root/.m2:/root/.m2'
 }
 }
stages {
stage('Build') {
steps {
sh 'mvn -B -DskipTests clean package'
}
}
}
}
