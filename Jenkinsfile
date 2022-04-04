node{
def mavenHome = tool name: "maven3.8.4"
//Checkout Stage
stage( 'checkoutCode'){
git branch: 'development', credentialsId: 'f5f1c6e6-e02a-473f-89bd-9f5afd1ffdcf', url: 'https://github.com/Devops-automation-janbatch/maven-web-application.git'
}
//Build Stage
stage( 'Build'){
sh "$mavenHome/bin/mvn clean package"
}
/*
 //Generate sonarqube report
stage( 'SonarQubeReport'){
sh "$mavenHome/bin/mvn clean package sonar:sonar"
}
//Upload artifact into artifactory repo
stage ( 'Upload Artifact into repo'){
sh "$mavenHome/bin/mvn deploy "
}
stage( 'Deploy into Tomcat server' ){
sshagent(['d7df8ec6-2754-4831-9ecf-dab4b7b162aa']) {
 sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.111.168.102:/opt/apache-tomcat-9.0.60/webapps"  
}
}
*/
}//Node Closing
