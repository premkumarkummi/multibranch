node('built-in') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/premkumarkummi/multibranch.git'
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
      sh 'echo "shree boss have a 1 lack money so boss is full free now i dont have money wt to do" '
     }
	stage('Continous Delivery') 
     {
      sh 'scp   /home/ubuntu/.jenkins/workspace/multi_project_loans/webapp/target/webapp.war ubuntu@172.31.42.147:/var/lib/tomcat9/webapps/prodenv.war'
     }
}
