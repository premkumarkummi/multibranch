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
}
