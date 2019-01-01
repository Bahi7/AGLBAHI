pipeline {
agent any
tools {
maven 'MVN3'
jdk 'JDK11'
}
stages{
stage ('Build'){
steps {
bat 'mvn install'
}
post {
success {
junit 'target/surefire-reports/**/*.xml'
}
}
}
}
}
