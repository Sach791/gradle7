pipeline{
agent any

tools{
gradle 'Gradle'
jdk 'JDK'
}

stages{

stage('checkout'){
steps{
git branch:'master',url:'https://github.com/Sach791/gradle7.git'
}
}
stage('build'){
steps{
sh 'gradle build'
}
}
stage('test'){
steps{
sh 'gradle test'
}
}
stage('Run Application'){
steps{
sh 'gradle run'
}
}
}
post{
success{
echo 'build and deployment successful'
}
failure{
echo 'deployment failed!'
}
}
}

