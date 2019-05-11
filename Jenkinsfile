pipeline{
agent any
stages{
stage('SCM checkout'){
git 'https://github.com/mg2412/maven-project.git'
}
stage('maven test'){
steps{
withMaven(maven: 'localMaven'){
sh 'mvn test'
}
}
}
stage('maven package'){
steps{
withMaven(maven: 'localMaven'){
sh 'mvn package'
}
}
}
stage('maven install'){
steps{
withMaven(maven: 'localMaven'){
sh 'mvn install'
}
}
}
}
}
