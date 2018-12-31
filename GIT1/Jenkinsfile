pipeline {
agent any
tools {
maven 'Maven 3.5.2'
jdk 'jdk-11.0.1'
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
