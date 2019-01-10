pipeline
{
    agent any
    stages
    {
        stage('ContDownload')
        {
            steps
            {
                git 'https://github.com/demoglot/java.git'
            }
        }
        stage('ContBuild')
        {
            steps
            {
                sh 'mvn package'
            }
        }
        stage('ContDeployment')
        {
            steps
            {
                sh 'scp /var/lib/jenkins/workspace/pipe/target/CounterWebApp.war root@13.233.104.227:/root/tomcat/webapps/raju.war'
            }
        }
    }
}
