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
	stage('Continuous deployment') 
	 {
    sh 'scp /home/ubuntu/.jenkins/workspace/multi_project_master/webapp/target/webapp.war ubuntu@172.31.37.35:/var/lib/tomcat9/webapps/qaenv.war'
	 }
	stage('Continuous testing')
	{
      sh 'echo "my lover is always lucky" '
        }
	stage('Continous Delivery') 
     {
      sh 'scp   /home/ubuntu/.jenkins/workspace/multi_project_loans/webapp/target/webapp.war ubuntu@172.31.42.147:/var/lib/tomcat9/webapps/prodenv.war'
     }
}
