pipeline{
agent any
tools{
gradle 'Gradle'
jdk 'JDK17'
}
stages{
stage('Checkout'){
steps{
git branch:'main',url:'https://github.com/dhanushV360/gradlejenkins.git'
}
}
stage('Build'){
steps{
sh'gradle build'
}
}
stage('Test'){
steps{
sh'gradle test'
}
}
stage('Run Application'){
steps{
sh'gradle run'
}
}
}
post{
success{
echo'Build and deployment successful!'
}
failure{
echo 'Build failed!'
}
}
}

