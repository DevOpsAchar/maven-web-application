node{

  def mavenHome = tool name: 'Maven3.8.5'
  
  echo "The Job Name is: ${env.JOB_NAME}"
  echo "The Build NUmber is: ${env.BUILD_NUMBER}"
  echo "The Node Name is: ${env.NODE_NAME}"
  
//Checkout Code Stage
stage('CheckoutCode'){
git branch: 'development', credentialsId: '4ca03b7f-8e21-401a-b5df-7e52f888fa8b', url: 
'https://github.com/Vishwakar12/maven-web-application.git'
}

//Build{
stage('Build'){
sh "${mavenHome}/bin/mvn clean package"
}

    /*
//Execute Sonarqube Report
stage('ExecuteSonarQubeReport'){
sh "${mavenHome}/bin/mvn sonar:sonar"
}

//UploadArtifacts into nexus
stage('UploadArtifactsIntoNexus'){
sh "${mavenHome}/bin/mvn deploy"
}

//Deploy App Into Tomatcat Server
stage('DeployApp'){
sshagent(['c7ede373-19c4-4fbc-ba20-166239c14b24']){
sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2user@172.31.40.115:/opt/apache-tomcat-9.0.68/webapps"
}
}

*/

}//node
   
 
