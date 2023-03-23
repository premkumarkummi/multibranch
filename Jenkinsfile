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
   
}
