node('built-in') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continous Deployment') 
       {
      sh 'scp   /home/ubuntu/.jenkins/workspace/multi_project_loans/webapp/target/webapp.war ubuntu@172.31.37.35:/var/lib/tomcat9/webapps/qaenv.war'
       }
    stage('Continous Testing') 
     {
      sh 'echo "do something in life then only u cat anything in life" '
     }
stage('Continous Delivery') 
     {
      sh 'scp   /home/ubuntu/.jenkins/workspace/multi_project_loans/webapp/target/webapp.war ubuntu@172.31.42.147:/var/lib/tomcat9/webapps/prodenv.war'
     }
}
