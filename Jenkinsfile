pipeline {
 agent {
 docker {
  image 'arm32v7/maven:3.6-jdk-8-slim' 
  args '-v /root/.m2:/root/.m2 -u 0:0'
 }
 }
stages {
stage('Build') {
steps {
sh 'mvn -B -DskipTests clean package'
}
}
stage('Test') {
steps {
sh 'mvn test'
}
post {
always {
junit 'target/surefire-reports/*.xml'
}
}
}
}
}
