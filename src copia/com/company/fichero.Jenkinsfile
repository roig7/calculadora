pipeline {
agent any
stages {
stage('Compile') {
steps {
sh 'mvn -B -DskipTests clean package'
}
}
stage('Unit test') {
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